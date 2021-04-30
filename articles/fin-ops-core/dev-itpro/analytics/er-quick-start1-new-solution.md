---
title: Navrhněte nové řešení ER pro tisk vlastní sestavy
description: Toto téma vysvětluje, jak navrhnout řešení elektronického výkaznictví (ER) pro tisk vlastní sestavy.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a3e0e4a8389fdd6580f66004d86ef4b1980dd9f
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891786"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="93e44-103">Navrhněte nové řešení ER pro tisk vlastní sestavy</span><span class="sxs-lookup"><span data-stu-id="93e44-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="93e44-104">Následující kroky vysvětlují, jak může uživatel v roli administrátora systému, vývojáře elektronických zpráv nebo funkčního konzultanta pro elektronické vykazování konfigurovat parametry rámce ER, navrhovat požadované konfigurace ER nového řešení ER pro přístup k datům konkrétní obchodní domény, a vygenerovat vlastní přehled ve formátu Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="93e44-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="93e44-105">Tyto kroky lze provést v rámci společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="93e44-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="93e44-106">Konfigurace architektury ER</span><span class="sxs-lookup"><span data-stu-id="93e44-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="93e44-107">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="93e44-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="93e44-108">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="93e44-109">Kontrola seznamu poskytovatelů konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="93e44-110">Přidání nového poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="93e44-111">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="93e44-112">Návrh datového modelu specifického pro doménu</span><span class="sxs-lookup"><span data-stu-id="93e44-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="93e44-113">Import nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="93e44-114">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="93e44-115">Pojmenování datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="93e44-116">Přidání pole datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="93e44-117">Dokončení návrhu datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="93e44-118">Návrh mapování modelu pro konfigurovaný datový model</span><span class="sxs-lookup"><span data-stu-id="93e44-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="93e44-119">Import nové konfigurace mapového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="93e44-120">Vytvoření nové konfigurace mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="93e44-121">Návrh nového komponentu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="93e44-122">Přidání zdroje dat pro přístup k aplikačním tabulkám</span><span class="sxs-lookup"><span data-stu-id="93e44-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="93e44-123">Přidání zdroje dat pro přístup k výčtům aplikací</span><span class="sxs-lookup"><span data-stu-id="93e44-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="93e44-124">Přidání štítků ER a vygenerování sestavy ve specifikovaném jazyce</span><span class="sxs-lookup"><span data-stu-id="93e44-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="93e44-125">Přidání zdroje dat pro transformaci výsledků porovnání hodnot výčtu k textové hodnotě</span><span class="sxs-lookup"><span data-stu-id="93e44-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="93e44-126">Navázání zdroje dat na pole zdrojů dat</span><span class="sxs-lookup"><span data-stu-id="93e44-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="93e44-127">Dokončení návrhu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="93e44-128">Navrhněte šablonu pro vlastní sestavu</span><span class="sxs-lookup"><span data-stu-id="93e44-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="93e44-129">Návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="93e44-130">Import navrženého formátu konfigurace</span><span class="sxs-lookup"><span data-stu-id="93e44-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="93e44-131">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="93e44-132">Import šablony sestavy</span><span class="sxs-lookup"><span data-stu-id="93e44-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="93e44-133">Konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="93e44-134">Definice datové vazby pro název sestavy</span><span class="sxs-lookup"><span data-stu-id="93e44-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="93e44-135">Kontrola zdrojových data modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="93e44-136">Vázání prvků formátu na pole zdroje dat</span><span class="sxs-lookup"><span data-stu-id="93e44-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="93e44-137">Spuštění navrženého formátu z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="93e44-138">Vylaďte navržený formát</span><span class="sxs-lookup"><span data-stu-id="93e44-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="93e44-139">Upravte formát a změňte název generovaného dokumentu</span><span class="sxs-lookup"><span data-stu-id="93e44-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="93e44-140">Upravte formát a změňte pořadí otázek</span><span class="sxs-lookup"><span data-stu-id="93e44-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="93e44-141">Spuštění upraveného formátu z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="93e44-142">Dokončete návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="93e44-143">Vytvořte artefakty aplikace a pojmenujte navrženou sestavu</span><span class="sxs-lookup"><span data-stu-id="93e44-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="93e44-144">Úprava zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="93e44-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="93e44-145">Přidejte třídu datového kontraktu</span><span class="sxs-lookup"><span data-stu-id="93e44-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="93e44-146">Přidejte třídu tvůrce uživatelského rozhraní</span><span class="sxs-lookup"><span data-stu-id="93e44-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="93e44-147">Přidejte třídu poskyovatele dat</span><span class="sxs-lookup"><span data-stu-id="93e44-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="93e44-148">Přidejte soubor štítků</span><span class="sxs-lookup"><span data-stu-id="93e44-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="93e44-149">Přidejte třídu služby sestav</span><span class="sxs-lookup"><span data-stu-id="93e44-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="93e44-150">Přidejte třídu kontrolera sestav</span><span class="sxs-lookup"><span data-stu-id="93e44-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="93e44-151">Přidejte položku nabídky</span><span class="sxs-lookup"><span data-stu-id="93e44-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="93e44-152">Přidejte položku nabídky k nabídce</span><span class="sxs-lookup"><span data-stu-id="93e44-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="93e44-153">Sestavte Visual Studio projekt</span><span class="sxs-lookup"><span data-stu-id="93e44-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="93e44-154">Spusťte formát z aplikace</span><span class="sxs-lookup"><span data-stu-id="93e44-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="93e44-155">Vylaďte navržené řešení ER</span><span class="sxs-lookup"><span data-stu-id="93e44-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="93e44-156">Úprava mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="93e44-157">Přidání zdroje dat pro přístup k objektu kontraktu dat</span><span class="sxs-lookup"><span data-stu-id="93e44-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="93e44-158">Přidejte zdroj dat pro přístup k záznamům mapování formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="93e44-159">Přidejte zdroj dat pro přístup k záznam mapování běžícího formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="93e44-160">Zadejte název datového modelu běžícího formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="93e44-161">Dokončení návrhu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="93e44-162">Změna formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="93e44-163">Přidat nový prvek formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="93e44-164">Vázání přidaného prvku formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="93e44-165">Dokončete návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="93e44-166">Spusťte formát z aplikace</span><span class="sxs-lookup"><span data-stu-id="93e44-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="93e44-167">Spusťte formát z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="93e44-168">Konfigurace cílového formátu pro náhled na obrazovce</span><span class="sxs-lookup"><span data-stu-id="93e44-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="93e44-169">Spusťte formát z aplikace a zobrazte jej jako dokument PDF</span><span class="sxs-lookup"><span data-stu-id="93e44-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="93e44-170">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="93e44-170">Additional resources</span></span>](#References)

<span data-ttu-id="93e44-171">V tomto příkladu vytvoříte nové řešení ER pro modul [Dotazník](../../../human-resources/hr-learning-questionnaires.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="93e44-172">Toto nové řešení ER vám umožňuje navrhnout sestavu pomocí listu Microsoft Excel jako šablony.</span><span class="sxs-lookup"><span data-stu-id="93e44-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="93e44-173">Poté můžete vygenerovat **Dotazník** sestavu ve formátu Excel nebo PDF, kromě generování existující zprávy SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="93e44-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="93e44-174">Novou sestavu můžete také na požádání upravit později.</span><span class="sxs-lookup"><span data-stu-id="93e44-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="93e44-175">Není nutné žádné kódování.</span><span class="sxs-lookup"><span data-stu-id="93e44-175">No coding is required.</span></span>

1. <span data-ttu-id="93e44-176">Chcete-li spustit stávající sestavu, přejděte na **Dotazník** \> **Design** \> **Sestava dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="93e44-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Výběrem položky nabídky Přehled dotazníků v modulu Dotazník spustíte existující sestavu SSRS](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="93e44-178">V dialogovém okně **Sestava dotazníků** zadejte kritéria výběru.</span><span class="sxs-lookup"><span data-stu-id="93e44-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="93e44-179">Použijte filtr tak, aby přehled obsahoval pouze **SBCCrsExam** dotazník.</span><span class="sxs-lookup"><span data-stu-id="93e44-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![V dialogovém okně Sestava dotazníků zadejte kritéria výběru.](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="93e44-181">Následující obrázek ukazuje generovanou verzi zprávy SSRS pro dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Generovaná SSRS sestava](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="93e44-183">Konfigurace rámce ER</span><span class="sxs-lookup"><span data-stu-id="93e44-183">Configure the ER framework</span></span>

<span data-ttu-id="93e44-184">Jako uživatel v roli vývojáře elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER, abyste mohli začít používat rámec ER k navrhovánínového ER řešení.</span><span class="sxs-lookup"><span data-stu-id="93e44-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="93e44-185">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="93e44-185">Configure ER parameters</span></span>

1. <span data-ttu-id="93e44-186">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="93e44-187">V pracovním prostoru **Elektronické sestavy** vyberte **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="93e44-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="93e44-188">Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="93e44-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="93e44-189">Na kartě **Přílohy** natavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="93e44-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="93e44-190">V poli **Konfigurace** vyberte pro společnost **USMF** typ **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="93e44-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="93e44-191">V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.</span><span class="sxs-lookup"><span data-stu-id="93e44-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="93e44-192">Další informace o parametrech ER najdete v tématu [Konfigurace rámce ER](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="93e44-193">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="93e44-194">U každé označené konfigurace ER je vyznačen jako vlastník poskytovatel konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="93e44-195">Než začnete přidávat nebo upravovat konfigurace ER, musíte proto aktivovat poskytovatele konfigurace ER v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="93e44-196">Pouze vlastník konfigurace ER může konfiguraci upravovat.</span><span class="sxs-lookup"><span data-stu-id="93e44-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="93e44-197">Konfiguraci ER proto můžete upravovat teprve poté, co je příslušná konfigurace ER aktivována v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="93e44-198">Kontrola seznamu poskytovatelů konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="93e44-199">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="93e44-200">V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Poskytovatelé konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="93e44-201">Na stránce **Poskytovatelé konfigurace** má záznam každé konfigurace jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="93e44-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="93e44-202">Zkontrolujte obsah této stránky.</span><span class="sxs-lookup"><span data-stu-id="93e44-202">Review the contents of this page.</span></span> <span data-ttu-id="93e44-203">Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#ActivateProvider), přeskočte.</span><span class="sxs-lookup"><span data-stu-id="93e44-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="93e44-204">Přidání nového poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="93e44-205">Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93e44-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="93e44-206">Do pole **Název** zadejte **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="93e44-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="93e44-207">Do pole **Internetová adresa** zadejte `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="93e44-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="93e44-208">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="93e44-209">Aktivace poskytovatele konfigurace ER</span><span class="sxs-lookup"><span data-stu-id="93e44-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="93e44-210">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="93e44-211">V **Elektronickém výkaznictí** vyberte **Litware, Inc.** pro vašeho poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="93e44-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="93e44-212">Vyberte **Nastavit jako aktivní**.</span><span class="sxs-lookup"><span data-stu-id="93e44-212">Select **Set active**.</span></span>

<span data-ttu-id="93e44-213">Další informace o poskytovatelích konfigurací ER naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="93e44-214">Návrh datového modelu specifického pro doménu</span><span class="sxs-lookup"><span data-stu-id="93e44-214">Design a domain-specific data model</span></span>

<span data-ttu-id="93e44-215">Musíte vytvořit novou konfiguraci ER obsahující součást [datový model](general-electronic-reporting.md#data-model-and-model-mapping-components) pro obchodní doménu **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="93e44-216">Tento datový model bude později použit jako zdroj dat, když navrhujete formát ER pro generování sestavy **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="93e44-217">Dokončením kroků v části [Importujte novou konfiguraci datového modelu](#ImportDataModel) můžete importovat požadovanou konfiguraci datového modelu z poskytnutého souboru XML.</span><span class="sxs-lookup"><span data-stu-id="93e44-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="93e44-218">Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace datového modelu](#DesignDataModel), chcete-li navrhnout tento datový model od začátku.</span><span class="sxs-lookup"><span data-stu-id="93e44-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="93e44-219">Import nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="93e44-220">Stáhněte si soubor [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) a uložte jej do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="93e44-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="93e44-221">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="93e44-222">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="93e44-223">V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="93e44-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="93e44-224">Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="93e44-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="93e44-225">Kliknutím na tlačítko **OK** importujte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="93e44-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="93e44-226">Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace datového modelu](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="93e44-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="93e44-227">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="93e44-228">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="93e44-229">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="93e44-230">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="93e44-231">V rozevíracím dialogovém okně do pole **Název** zadejte **Model dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="93e44-232">Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="93e44-233">Pojmenování datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-233">Name the data model</span></span>

1. <span data-ttu-id="93e44-234">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="93e44-235">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="93e44-235">Select **Designer**.</span></span>
3. <span data-ttu-id="93e44-236">Na stránce **Návrhář datového modelu** v pevné záložce **Obecné**, do pole **Název** zadejte <a name="DataModeName"></a>**Dotazníky**.</span><span class="sxs-lookup"><span data-stu-id="93e44-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="93e44-237">Přidání nového pole datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-237">Add new data model fields</span></span>

1. <span data-ttu-id="93e44-238">Na stránce **Návrhář datového modelu** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="93e44-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="93e44-239">V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="93e44-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-240">Vyberte **Kořen modelu** jako typ nového uzlu.</span><span class="sxs-lookup"><span data-stu-id="93e44-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="93e44-241">Do pole **Název** zadejte řetězec <a name="RootDefinitionName"></a>**Kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="93e44-242">Kliknutím na **Přidat** přidáte nový uzel.</span><span class="sxs-lookup"><span data-stu-id="93e44-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="93e44-243">Tento kořenový popisovač se použije k poskytování dat pro sestavu **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="93e44-244">Jeden datový model může mít více popisovačů.</span><span class="sxs-lookup"><span data-stu-id="93e44-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="93e44-245">Každý popisovač může být určen pro jeden formát ER pro identifikaci dat, která jsou vyžadována pro generování sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="93e44-246">Znovu zvolte **Nový** a poté v rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="93e44-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-247">Vyberte **Podřízený aktivního uzlu** jako typ nového uzlu.</span><span class="sxs-lookup"><span data-stu-id="93e44-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="93e44-248">Do pole **Název** zadejte **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="93e44-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="93e44-249">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="93e44-250">Kliknutím na **Přidat** přidáte nové pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="93e44-251">Toto pole je vyžadováno pro předání názvu aktuální společnosti do sestavy ER, která používá tento datový model jako zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="93e44-252">Znovu zvolte **Nový** a poté v rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="93e44-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-253">Vyberte **Podřízený aktivního uzlu** jako typ nového uzlu.</span><span class="sxs-lookup"><span data-stu-id="93e44-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="93e44-254">Do pole **Název** zadejte **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="93e44-255">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="93e44-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="93e44-256">Kliknutím na **Přidat** přidáte nové pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="93e44-257">Toto pole bude použito pro předání seznamu dotazníků do sestavy ER, která používá tento datový model jako zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="93e44-258">Vyberte uzel **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="93e44-259">Stejným způsobem pokračujte v přidávání povinných polí upravitelného datového modelu, dokud nedokončíte následující strukturu datového modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="93e44-260">Cesta pole</span><span class="sxs-lookup"><span data-stu-id="93e44-260">Field path</span></span>                                                    | <span data-ttu-id="93e44-261">Datový typ</span><span class="sxs-lookup"><span data-stu-id="93e44-261">Data type</span></span>   | <span data-ttu-id="93e44-262">Označení pole / vrácená hodnota</span><span class="sxs-lookup"><span data-stu-id="93e44-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="93e44-263">Kořen</span><span class="sxs-lookup"><span data-stu-id="93e44-263">Root</span></span>                                                          |             | <span data-ttu-id="93e44-264">Referenční bod pro vyžádání údajů z dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="93e44-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="93e44-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="93e44-266">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-266">String</span></span>      | <span data-ttu-id="93e44-267">Název aktuální společnosti.</span><span class="sxs-lookup"><span data-stu-id="93e44-267">The name of the current company.</span></span> |
    | <span data-ttu-id="93e44-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="93e44-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="93e44-269">Záznam</span><span class="sxs-lookup"><span data-stu-id="93e44-269">Record</span></span>      | <span data-ttu-id="93e44-270">Podrobnosti o spuštění formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-270">Format execution details.</span></span> |
    | <span data-ttu-id="93e44-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="93e44-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="93e44-272">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-272">String</span></span>      | <span data-ttu-id="93e44-273">Název právě spuštěného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="93e44-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="93e44-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="93e44-275">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-275">Record list</span></span> | <span data-ttu-id="93e44-276">Seznam dotazníků</span><span class="sxs-lookup"><span data-stu-id="93e44-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="93e44-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="93e44-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="93e44-278">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-278">String</span></span>      | <span data-ttu-id="93e44-279">Stav aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="93e44-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="93e44-281">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-281">String</span></span>      | <span data-ttu-id="93e44-282">Kód aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="93e44-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="93e44-284">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-284">String</span></span>      | <span data-ttu-id="93e44-285">Popis aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="93e44-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="93e44-287">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-287">String</span></span>      | <span data-ttu-id="93e44-288">Typ aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="93e44-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="93e44-290">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-290">String</span></span>      | <span data-ttu-id="93e44-291">Číselné pořadí aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="93e44-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="93e44-293">Záznam</span><span class="sxs-lookup"><span data-stu-id="93e44-293">Record</span></span>      | <span data-ttu-id="93e44-294">Výsledné parametry aktuálního dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="93e44-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="93e44-296">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-296">String</span></span>      | <span data-ttu-id="93e44-297">Identifikační kód aktuální skupiny výsledků.</span><span class="sxs-lookup"><span data-stu-id="93e44-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="93e44-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="93e44-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="93e44-299">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-299">String</span></span>      | <span data-ttu-id="93e44-300">Popis aktuálnískupiny výsledků.</span><span class="sxs-lookup"><span data-stu-id="93e44-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="93e44-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="93e44-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="93e44-302">Reálný</span><span class="sxs-lookup"><span data-stu-id="93e44-302">Real</span></span>        | <span data-ttu-id="93e44-303">Maximální počet bodů, které lze získat.</span><span class="sxs-lookup"><span data-stu-id="93e44-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="93e44-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="93e44-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="93e44-305">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-305">Record list</span></span> | <span data-ttu-id="93e44-306">Seznam otázek pro aktuální dotazník.</span><span class="sxs-lookup"><span data-stu-id="93e44-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="93e44-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="93e44-308">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-308">Integer</span></span>     | <span data-ttu-id="93e44-309">Pořadové číslo aktuální kolekce odpovědí.</span><span class="sxs-lookup"><span data-stu-id="93e44-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="93e44-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="93e44-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="93e44-311">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-311">String</span></span>      | <span data-ttu-id="93e44-312">Identifikační kód aktuální otázky.</span><span class="sxs-lookup"><span data-stu-id="93e44-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="93e44-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="93e44-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="93e44-314">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-314">String</span></span>      | <span data-ttu-id="93e44-315">Příznak, který označuje, zda je třeba odpovědět na aktuální otázku.</span><span class="sxs-lookup"><span data-stu-id="93e44-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="93e44-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="93e44-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="93e44-317">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-317">String</span></span>      | <span data-ttu-id="93e44-318">Příznak, který označuje, zda je aktuální otázka primární.</span><span class="sxs-lookup"><span data-stu-id="93e44-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="93e44-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="93e44-320">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-320">Integer</span></span>     | <span data-ttu-id="93e44-321">Pořadové číslo aktuální otázky.</span><span class="sxs-lookup"><span data-stu-id="93e44-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="93e44-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="93e44-323">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-323">String</span></span>      | <span data-ttu-id="93e44-324">Text aktuální otázky.</span><span class="sxs-lookup"><span data-stu-id="93e44-324">The text of the current question.</span></span> |
    | <span data-ttu-id="93e44-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="93e44-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="93e44-326">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-326">Record list</span></span> | <span data-ttu-id="93e44-327">Seznam odpovědí pro aktuální otázku.</span><span class="sxs-lookup"><span data-stu-id="93e44-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="93e44-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="93e44-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="93e44-329">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-329">String</span></span>      | <span data-ttu-id="93e44-330">Příznak, který označuje, zda je aktuální odpověď správná.</span><span class="sxs-lookup"><span data-stu-id="93e44-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="93e44-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="93e44-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="93e44-332">Reálný</span><span class="sxs-lookup"><span data-stu-id="93e44-332">Real</span></span>        | <span data-ttu-id="93e44-333">Body, které získáte, když je vybrána aktuální odpověď.</span><span class="sxs-lookup"><span data-stu-id="93e44-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="93e44-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="93e44-335">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-335">Integer</span></span>     | <span data-ttu-id="93e44-336">Pořadové číslo aktuální odpovědi.</span><span class="sxs-lookup"><span data-stu-id="93e44-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="93e44-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="93e44-338">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-338">String</span></span>      | <span data-ttu-id="93e44-339">Text aktuální odpovědi.</span><span class="sxs-lookup"><span data-stu-id="93e44-339">The text of the current answer.</span></span> |

    <span data-ttu-id="93e44-340">Následující obrázek ukazuje dokončený upravitelný datový model na stránce **Návrhář datového modelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigurovaný datový model v návrháři datového modelu ER](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="93e44-342">Uložte změny.</span><span class="sxs-lookup"><span data-stu-id="93e44-342">Save your changes.</span></span>
8. <span data-ttu-id="93e44-343">Zavřete stránku **Návrhář datového modelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="93e44-344">Dokončení návrhu datového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="93e44-345">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-346">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="93e44-347">Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="93e44-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="93e44-348">Vyberte **Změnit stav** \> **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="93e44-349">Stav verze 1 této konfigurace se změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="93e44-350">Verzi 1 již nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="93e44-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="93e44-351">Tato verze obsahuje konfigurovaný datový model a lze ji použít jako základ pro další konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="93e44-352">Verze 2 této konfigurace je vytvořena a má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="93e44-353">Tuto verzi můžete upravit a tak upravit datový model **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Verze konfigurovatelné konfigurace ER na stránce Konfigurace](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="93e44-355">Další informace o verzích pro konfigurace ER viz [Přehled elektronického výkaznictví (ER)](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="93e44-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="93e44-356">Konfigurovaný datový model je vaše abstraktní reprezentace obchodní domény **Dotazník** a neobsahuje žádné vztahy k artefaktům, které jsou specifické pro službu Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="93e44-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="93e44-357">Návrh mapování modelu pro konfigurovaný datový model</span><span class="sxs-lookup"><span data-stu-id="93e44-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="93e44-358">Jako uživatel v roli Electronic Reporting Developer musíte vytvořit novou konfiguraci ER, která obsahuje [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) součást pro **Dotazník** datový model.</span><span class="sxs-lookup"><span data-stu-id="93e44-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="93e44-359">Protože tato komponenta implementuje nakonfigurovaný datový model pro Finance, je specifická pro Finance.</span><span class="sxs-lookup"><span data-stu-id="93e44-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="93e44-360">Komponentu mapování modelu musíte nakonfigurovat, abyste určili aplikační objekty, které musí být použity k vyplnění nakonfigurovaného datového modelu aplikačními daty za běhu.</span><span class="sxs-lookup"><span data-stu-id="93e44-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="93e44-361">K dokončení tohoto úkolu si musíte být vědomi podrobností o implementaci datové struktury systému **Dotazník** obchodní domény ve financích.</span><span class="sxs-lookup"><span data-stu-id="93e44-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="93e44-362">Dokončením kroků v [Importujte novou konfiguraci mapování](#ImportModelMapping) datového modelu v další části můžete importovat požadovanou konfiguraci mapování z poskytnutého souboru XML.</span><span class="sxs-lookup"><span data-stu-id="93e44-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="93e44-363">Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace mapování modelu](#CreateModelMapping), chcete-li navrhnout tento model mapování od začátku.</span><span class="sxs-lookup"><span data-stu-id="93e44-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="93e44-364">Import nové konfigurace mapového modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="93e44-365">Stáhněte si soubor [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) a uložte jej do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="93e44-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="93e44-366">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="93e44-367">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="93e44-368">V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="93e44-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="93e44-369">Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="93e44-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="93e44-370">Kliknutím na tlačítko **OK** importujte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="93e44-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="93e44-371">Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace mapování modelu](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="93e44-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="93e44-372">Vytvoření nové konfigurace mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="93e44-373">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-374">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="93e44-375">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="93e44-376">V rozevíracím dialogovém okně proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="93e44-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-377">V poli **Nový** vyberte **Mapování modelu založené na datovém modelu pro dotazníky**'.</span><span class="sxs-lookup"><span data-stu-id="93e44-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="93e44-378">Do pole **Název** zadejte **Mapování dotazníků**'.</span><span class="sxs-lookup"><span data-stu-id="93e44-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="93e44-379">V poli **Definice datového modelu** vyberte definici **Kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="93e44-380">Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="93e44-381">Návrh nového komponentu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="93e44-382">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Mapování dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="93e44-383">Výběrem možnosti **Návrhář** otevřete seznam mapování.</span><span class="sxs-lookup"><span data-stu-id="93e44-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="93e44-384">Vyberte mapování **Mapování dotazníků**, které bylo automaticky přidáno pro definici **Kořen**</span><span class="sxs-lookup"><span data-stu-id="93e44-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="93e44-385">Vybrat **Návrhář** k zahájení konfigurace vybraného mapování.</span><span class="sxs-lookup"><span data-stu-id="93e44-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="93e44-386">Nové mapování je automaticky přidáno pro definici **Kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="93e44-387">Toto mapování má směr **K modelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="93e44-388">Toto mapování lze proto použít k vyplnění datového modelu požadovanými daty.</span><span class="sxs-lookup"><span data-stu-id="93e44-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="93e44-389">Přidání zdroje dat pro přístup k aplikačním tabulkám</span><span class="sxs-lookup"><span data-stu-id="93e44-389">Add data sources to access application tables</span></span>

<span data-ttu-id="93e44-390">Pro přístup k aplikačním tabulkám, které obsahují podrobnosti dotazníku, musíte nakonfigurovat zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="93e44-391">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="93e44-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="93e44-392">Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMCollection, kde každý záznam představuje jeden dotazník:</span><span class="sxs-lookup"><span data-stu-id="93e44-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="93e44-393">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-394">V dialogovém okně do pole **Název** zadejte **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="93e44-395">Do pole **Tabulka** zadejte **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="93e44-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="93e44-396">Nastavte možnost **Zeptat se na dotaz** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="93e44-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="93e44-397">Poté budete moci určit možnosti [filtrování](../../fin-ops/get-started/advanced-filtering-query-options.md) pro tuto tabulku v dialogovém okně systémového dotazu za běhu.</span><span class="sxs-lookup"><span data-stu-id="93e44-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="93e44-398">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="93e44-399">V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulkové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="93e44-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="93e44-400">Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMQuestion, kde každý záznam představuje jednu otázku v dotazníku:</span><span class="sxs-lookup"><span data-stu-id="93e44-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="93e44-401">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-402">V dialogovém okně do pole **Název** zadejte **Otázka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="93e44-403">Do pole **Tabulka** zadejte **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="93e44-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="93e44-404">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="93e44-405">V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulkové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="93e44-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="93e44-406">Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMAnswer, kde každý záznam představuje jednu odpověď na otázku v dotazníku:</span><span class="sxs-lookup"><span data-stu-id="93e44-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="93e44-407">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-408">Do pole **Název** zadejte **Odpověď**.</span><span class="sxs-lookup"><span data-stu-id="93e44-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="93e44-409">Do pole **Tabulka** zadejte **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="93e44-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="93e44-410">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="93e44-411">V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="93e44-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="93e44-412">Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu tabulky KMQuestionResultGroup z každého záznamu nadřazené tabulky KMCollection:</span><span class="sxs-lookup"><span data-stu-id="93e44-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="93e44-413">V podokně **Zdroje dat** vyberte **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="93e44-414">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-414">Select **Add**.</span></span>
    3. <span data-ttu-id="93e44-415">V dialogovém okně do pole **Název** zadejte **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="93e44-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="93e44-416">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="93e44-417">V [Editoru vzorců ER](general-electronic-reporting-formula-designer.md), v poli **Vzorec**, zadejte **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** k použití vzájemných vztahů mezi tabulkami KMCollection a KMQQuestionesultGroup typu [cesta](er-formula-language.md#paths).</span><span class="sxs-lookup"><span data-stu-id="93e44-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="93e44-418">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="93e44-419">Vyberte **OK** pro přidání nového počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="93e44-420">V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="93e44-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="93e44-421">Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu dotazů tabulky KMQuestion z každého záznamu nadřazené tabulky KMCollectionQuestion:</span><span class="sxs-lookup"><span data-stu-id="93e44-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="93e44-422">V podokně **Zdroje dat** vyberte **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="93e44-423">Rozbalte uzel **\<Vztahy**, který obsahuje vzájemné vztahy mezi dvěma členy tabulky KMCollection.</span><span class="sxs-lookup"><span data-stu-id="93e44-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="93e44-424">Vyberte související tabulku **KMCollectionQuestion** a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="93e44-425">V dialogovém okně do pole **Název** zadejte **\$Otázka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="93e44-426">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="93e44-427">V editoru vzorců v poli **Vzorec** zadejte **FIRSTORNULL(FILTER (Question, Question.kmQuestionId = \@.kmQuestionId))** k vrácení příslušných záznamů otázek z tabulky KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="93e44-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="93e44-428">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="93e44-429">Vyberte **OK** pro přidání nového počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="93e44-430">V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="93e44-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="93e44-431">Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu odpovědí tabulky KMAnswer z každého záznamu nadřazené tabulky KMQuestion:</span><span class="sxs-lookup"><span data-stu-id="93e44-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="93e44-432">V podokně **Zdroje dat** vyberte **Dotazník.\<Relations.KMCollectionQuestion.\$Question** a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="93e44-433">V dialogovém okně do pole **Název** zadejte **\$Odpověď**.</span><span class="sxs-lookup"><span data-stu-id="93e44-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="93e44-434">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="93e44-435">V editoru vzorců v poli **Vzorec** zadejte **FIRSTORNULL(FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId))** k vrácení příslušných záznamů otázek z tabulky KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="93e44-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="93e44-436">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="93e44-437">Vyberte **OK** pro přidání nového počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="93e44-438">V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="93e44-439">Přidejte nový zdroj dat, který bude použit pro přístup k metodám tabulky CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="93e44-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="93e44-440">Všimněte si, že metoda **find()** této tabulky vrací záznam, který představuje společnost aktuální instance Finance, kterou se toto mapování nazývá v kontextu.</span><span class="sxs-lookup"><span data-stu-id="93e44-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="93e44-441">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-442">V dialogovém okně do pole **Název** zadejte **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="93e44-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="93e44-443">Do pole **Tabulka** zadejte **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="93e44-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="93e44-444">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="93e44-445">Přidání zdroje dat pro přístup k výčtům aplikací</span><span class="sxs-lookup"><span data-stu-id="93e44-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="93e44-446">Pro přístup k výčtu aplikací musíte nakonfigurovat zdroje dat a porovnat jejich hodnoty s hodnotami polí **Výčet** tabulky aplikací.</span><span class="sxs-lookup"><span data-stu-id="93e44-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="93e44-447">Výsledek porovnání musíte použít k vyplnění příslušných polí datového modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="93e44-448">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Výčet**.</span><span class="sxs-lookup"><span data-stu-id="93e44-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="93e44-449">Přidejte nový zdroj dat, který bude použit pro přístup k hodnotám výčtu **EnumAppNoYes**:</span><span class="sxs-lookup"><span data-stu-id="93e44-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="93e44-450">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-451">V dialogovém okně do pole **Název** zadejte **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="93e44-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="93e44-452">Do pole **Výčet** zadejte **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="93e44-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="93e44-453">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="93e44-454">V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Výčet**.</span><span class="sxs-lookup"><span data-stu-id="93e44-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="93e44-455">Přidejte nový zdroj dat, který bude použit pro přístup k hodnotám výčtu **KMCollectionQuestionMode**:</span><span class="sxs-lookup"><span data-stu-id="93e44-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="93e44-456">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-457">V rozevíracím dialogovém okně do pole **Název** zadejte **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="93e44-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="93e44-458">Do pole **Výčet** zadejte **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="93e44-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="93e44-459">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="93e44-460">Přidání štítků ER a vygenerování sestavy ve specifikovaném jazyce</span><span class="sxs-lookup"><span data-stu-id="93e44-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="93e44-461">Můžete přidat popisky ER a nakonfigurovat některé zdroje dat tak, aby vrátily hodnoty, které závisí na jazyce, který je definován v kontextu volání mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="93e44-462">Na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte **Odpověď** a poté zvolte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="93e44-463">Aktivujte pole **Popisek**.</span><span class="sxs-lookup"><span data-stu-id="93e44-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="93e44-464">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-464">Select **Translate**.</span></span>
4. <span data-ttu-id="93e44-465">V dialogovém okně **Překlad textu** proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="93e44-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-466">Do pole **ID popisku** zadejte **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="93e44-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="93e44-467">Do pole **Text ve výchozím jazyce** zadejte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="93e44-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="93e44-468">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="93e44-469">Do pole **ID popisku** zadejte **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="93e44-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="93e44-470">Do pole **Text ve výchozím jazyce** zadejte **Ne**.</span><span class="sxs-lookup"><span data-stu-id="93e44-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="93e44-471">Vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-471">Select **Translate**.</span></span>

5. <span data-ttu-id="93e44-472">Zavřete **Překlad textu** dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="93e44-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="93e44-473">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-473">Select **Cancel**.</span></span>

![Přidejte označení ER pro mapování upravitelného modelu](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="93e44-475">Zadali jste označení ER pouze pro výchozí jazyk.</span><span class="sxs-lookup"><span data-stu-id="93e44-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="93e44-476">Informace o tom, jak lze štítky ER překládat do jiných jazyků, naleznete v části [Navrhujte vícejazyčné zprávy](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="93e44-477">Přidání zdroje dat pro transformaci výsledků porovnání hodnot výčtu k textové hodnotě</span><span class="sxs-lookup"><span data-stu-id="93e44-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="93e44-478">Protože je nutné transformovat výsledky porovnání mezi hodnotami výčtu a textovými hodnotami několikrát pro různé zdroje, je vhodné tuto logiku nakonfigurovat jako jediný zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="93e44-479">Chcete-li však tento zdroj dat znovu použít, musíte jej nakonfigurovat jako parametrizovaný zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="93e44-480">Další informace naleznete v [Podpora parametrizovaných volání datových zdrojů elektronického výkaznictví typu vypočítaného pole](er-calculated-field-type.md)</span><span class="sxs-lookup"><span data-stu-id="93e44-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="93e44-481">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Obecné\\Prázdný kontejner**.</span><span class="sxs-lookup"><span data-stu-id="93e44-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="93e44-482">Přidání nového zdroje dat typu kontejner:</span><span class="sxs-lookup"><span data-stu-id="93e44-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="93e44-483">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="93e44-484">V dialogovém okně do pole **Název** zadejte **Pomocník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="93e44-485">Vyberte **OK** pro přidání nového zdroje dat typu kontejner.</span><span class="sxs-lookup"><span data-stu-id="93e44-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="93e44-486">V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="93e44-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="93e44-487">Přidání nového zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="93e44-487">Add a new data source:</span></span>

    1. <span data-ttu-id="93e44-488">V podokně **Zdroje dat** vyberte **Pomocník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="93e44-489">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-489">Select **Add**.</span></span>
    3. <span data-ttu-id="93e44-490">V dialogovém okně do pole **Název** zadejte **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="93e44-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="93e44-491">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="93e44-492">V editoru vzorců vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="93e44-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="93e44-493">Chcete-li určit měrnou jednotku pro konfigurovaný výraz, postupujte takto</span><span class="sxs-lookup"><span data-stu-id="93e44-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="93e44-494">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="93e44-494">Select **New**.</span></span>
        2. <span data-ttu-id="93e44-495">V dialogovém okně do pole **Název** zadejte **Argument**.</span><span class="sxs-lookup"><span data-stu-id="93e44-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="93e44-496">V poli **Typ** vyberte datový typ **Logický**.</span><span class="sxs-lookup"><span data-stu-id="93e44-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="93e44-497">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-497">Select **OK**.</span></span>

    7. <span data-ttu-id="93e44-498">Do pole **Vzorec** zadejte **IF (Argument = true, \@"GER\_LABEL: PositiveAnswer", \@"GER\_LABEL: NegativeAnswer ")** pro vrácení textu příslušného označení ER, v závislosti na jazyce prováděcího kontextu a hodnotě zadaného parametru.</span><span class="sxs-lookup"><span data-stu-id="93e44-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="93e44-499">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="93e44-500">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-500">Select **OK** to add the new data source.</span></span>

![Konfigurovaný model mapování v návrháři mapového modelu ER](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="93e44-502">Navázání zdroje dat na pole zdrojů dat</span><span class="sxs-lookup"><span data-stu-id="93e44-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="93e44-503">Konfigurované zdroje dat musíte svázat s poli datového modelu a určit, jak bude datový model vyplněn aplikačními daty za běhu.</span><span class="sxs-lookup"><span data-stu-id="93e44-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="93e44-504">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="93e44-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="93e44-505">V podokně **Zdroje dat** rozbalte **CompanyInfo** a poté postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="93e44-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="93e44-506">Rozbalte **CompanyInfo.find()** uzel, který představuje **find()** metodu tabulky CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="93e44-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="93e44-507">Vyberte **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="93e44-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="93e44-508">Vyberte **Navázat** k vyplnění názvu společnosti, který nakonfigurovaný model mapování volá v kontextu za běhu.</span><span class="sxs-lookup"><span data-stu-id="93e44-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="93e44-509">V podokně **Datový model** vyberte **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="93e44-510">V podokně **Zdroje dat** vyberte **Dotazník** a poté vyberte **Navázat** k vyplnění záznamu dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="93e44-511">V podokně **Datový model** rozbalte **Questionnaire** a poté postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="93e44-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="93e44-512">V podokně **Datový model** vyberte **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="93e44-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="93e44-513">V podokně **Datový model** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="93e44-514">Do pole **Vzorec** zadejte **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** k vyplnění textově závislého a jazykově závislého výsledku porovnání mezi hodnotami výčtu.</span><span class="sxs-lookup"><span data-stu-id="93e44-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="93e44-515">Stejným způsobem pokračujte ve vázání zdrojů dat na pole datového modelu, dokud nedosáhnete následujícího výsledku.</span><span class="sxs-lookup"><span data-stu-id="93e44-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="93e44-516">Cesta pole</span><span class="sxs-lookup"><span data-stu-id="93e44-516">Field path</span></span>                                              | <span data-ttu-id="93e44-517">Datový typ</span><span class="sxs-lookup"><span data-stu-id="93e44-517">Data type</span></span>   | <span data-ttu-id="93e44-518">Akce</span><span class="sxs-lookup"><span data-stu-id="93e44-518">Action</span></span> | <span data-ttu-id="93e44-519">Výraz vazby</span><span class="sxs-lookup"><span data-stu-id="93e44-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="93e44-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="93e44-520">CompanyName</span></span>                                             | <span data-ttu-id="93e44-521">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-521">String</span></span>      | <span data-ttu-id="93e44-522">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-522">Bind</span></span>   | <span data-ttu-id="93e44-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="93e44-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="93e44-524">Dotazník</span><span class="sxs-lookup"><span data-stu-id="93e44-524">Questionnaire</span></span>                                           | <span data-ttu-id="93e44-525">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-525">Record list</span></span> | <span data-ttu-id="93e44-526">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-526">Bind</span></span>   | <span data-ttu-id="93e44-527">Dotazník</span><span class="sxs-lookup"><span data-stu-id="93e44-527">Questionnaire</span></span> |
    | <span data-ttu-id="93e44-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="93e44-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="93e44-529">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-529">String</span></span>      | <span data-ttu-id="93e44-530">Úpravy</span><span class="sxs-lookup"><span data-stu-id="93e44-530">Edit</span></span>   | <span data-ttu-id="93e44-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="93e44-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="93e44-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="93e44-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="93e44-533">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-533">String</span></span>      | <span data-ttu-id="93e44-534">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-534">Bind</span></span>   | <span data-ttu-id="93e44-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="93e44-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="93e44-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="93e44-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="93e44-537">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-537">String</span></span>      | <span data-ttu-id="93e44-538">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-538">Bind</span></span>   | <span data-ttu-id="93e44-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="93e44-539">\@.Description</span></span> |
    | <span data-ttu-id="93e44-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="93e44-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="93e44-541">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-541">String</span></span>      | <span data-ttu-id="93e44-542">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-542">Bind</span></span>   | <span data-ttu-id="93e44-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="93e44-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="93e44-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="93e44-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="93e44-545">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-545">String</span></span>      | <span data-ttu-id="93e44-546">Úpravy</span><span class="sxs-lookup"><span data-stu-id="93e44-546">Edit</span></span>   | <span data-ttu-id="93e44-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="93e44-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="93e44-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="93e44-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="93e44-549">EnumAppQuestionOrder.Random, "Random (procento v dotazníku)",</span><span class="sxs-lookup"><span data-stu-id="93e44-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="93e44-550">EnumAppQuestionOrder.RandomGroup, "Random (procento ve skupině výsledků)",</span><span class="sxs-lookup"><span data-stu-id="93e44-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="93e44-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="93e44-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="93e44-552">"")</span><span class="sxs-lookup"><span data-stu-id="93e44-552">"")</span></span> |
    | <span data-ttu-id="93e44-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="93e44-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="93e44-554">Záznam</span><span class="sxs-lookup"><span data-stu-id="93e44-554">Record</span></span>      |        | |
    | <span data-ttu-id="93e44-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="93e44-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="93e44-556">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-556">String</span></span>      | <span data-ttu-id="93e44-557">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-557">Bind</span></span>   | <span data-ttu-id="93e44-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="93e44-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="93e44-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="93e44-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="93e44-560">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-560">String</span></span>      | <span data-ttu-id="93e44-561">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-561">Bind</span></span>   | <span data-ttu-id="93e44-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="93e44-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="93e44-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="93e44-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="93e44-564">Reálný</span><span class="sxs-lookup"><span data-stu-id="93e44-564">Real</span></span>        | <span data-ttu-id="93e44-565">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-565">Bind</span></span>   | <span data-ttu-id="93e44-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="93e44-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="93e44-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="93e44-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="93e44-568">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-568">Record list</span></span> | <span data-ttu-id="93e44-569">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-569">Bind</span></span>   | <span data-ttu-id="93e44-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="93e44-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="93e44-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="93e44-572">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-572">Integer</span></span>     | <span data-ttu-id="93e44-573">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-573">Bind</span></span>   | <span data-ttu-id="93e44-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="93e44-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="93e44-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="93e44-576">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-576">String</span></span>      | <span data-ttu-id="93e44-577">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-577">Bind</span></span>   | <span data-ttu-id="93e44-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="93e44-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="93e44-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="93e44-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="93e44-580">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-580">String</span></span>      | <span data-ttu-id="93e44-581">Úpravy</span><span class="sxs-lookup"><span data-stu-id="93e44-581">Edit</span></span>   | <span data-ttu-id="93e44-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="93e44-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="93e44-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="93e44-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="93e44-584">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-584">String</span></span>      | <span data-ttu-id="93e44-585">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-585">Bind</span></span>   | <span data-ttu-id="93e44-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="93e44-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="93e44-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="93e44-588">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-588">Integer</span></span>     | <span data-ttu-id="93e44-589">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-589">Bind</span></span>   | <span data-ttu-id="93e44-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="93e44-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="93e44-592">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-592">String</span></span>      | <span data-ttu-id="93e44-593">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-593">Bind</span></span>   | <span data-ttu-id="93e44-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="93e44-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="93e44-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="93e44-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="93e44-596">Seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="93e44-596">Record list</span></span> | <span data-ttu-id="93e44-597">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-597">Bind</span></span>   | <span data-ttu-id="93e44-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="93e44-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="93e44-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="93e44-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="93e44-600">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-600">String</span></span>      | <span data-ttu-id="93e44-601">Úpravy</span><span class="sxs-lookup"><span data-stu-id="93e44-601">Edit</span></span>   | <span data-ttu-id="93e44-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="93e44-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="93e44-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="93e44-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="93e44-604">Reálný</span><span class="sxs-lookup"><span data-stu-id="93e44-604">Real</span></span>        | <span data-ttu-id="93e44-605">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-605">Bind</span></span>   | <span data-ttu-id="93e44-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="93e44-606">\@.point</span></span> |
    | <span data-ttu-id="93e44-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="93e44-608">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="93e44-608">Integer</span></span>     | <span data-ttu-id="93e44-609">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-609">Bind</span></span>   | <span data-ttu-id="93e44-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="93e44-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="93e44-612">Řetězec</span><span class="sxs-lookup"><span data-stu-id="93e44-612">String</span></span>      | <span data-ttu-id="93e44-613">Vazba</span><span class="sxs-lookup"><span data-stu-id="93e44-613">Bind</span></span>   | <span data-ttu-id="93e44-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="93e44-614">\@.text</span></span> |

    <span data-ttu-id="93e44-615">Následující obrázek ukazuje konečný stav konfigurovaných mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Plně konfigurovaný model mapování v návrháři mapového modelu ER](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="93e44-617">Uložte změny.</span><span class="sxs-lookup"><span data-stu-id="93e44-617">Save your changes.</span></span>
8. <span data-ttu-id="93e44-618">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="93e44-619">Dokončení návrhu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="93e44-620">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-621">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Mapování dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="93e44-622">Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="93e44-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="93e44-623">Vyberte **Změnit stav** \> **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="93e44-624">Stav verze 1.1 této konfigurace se změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="93e44-625">Verzi 1.1 již nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="93e44-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="93e44-626">Tato verze obsahuje konfigurovaný model mapování a lze ji použít jako základ pro další konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="93e44-627">Verze 1.2 této konfigurace je vytvořena a má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="93e44-628">Tuto verzi můžete upravit a tak upravit konfiguraci **Mapování dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Verze konfigurovatelné konfigurace ER na stránce Konfigurace](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="93e44-630">Konfigurované mapování modelu je vaše implementace abstraktního datového modelu specifického pro Finance, který představuje obchodní doménu **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="93e44-631">Navrhněte šablonu pro vlastní sestavu</span><span class="sxs-lookup"><span data-stu-id="93e44-631">Design a template for a custom report</span></span>

<span data-ttu-id="93e44-632">Architektura elektronického výkaznictví používá předdefinované šablony ve formátech Microsoft Office (sešity aplikace Excel nebo dokumenty aplikace Word).</span><span class="sxs-lookup"><span data-stu-id="93e44-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="93e44-633">Při generování požadované sestavy je šablona podle požadovaných datových toků vyplněna požadovanými daty.</span><span class="sxs-lookup"><span data-stu-id="93e44-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="93e44-634">Proto musíte nejprve vytvořit šablonu pro vlastní sestavu.</span><span class="sxs-lookup"><span data-stu-id="93e44-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="93e44-635">Tato šablona musí být navržena jako sešit aplikace Excel, jehož struktura představuje rozložení vlastní sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="93e44-636">Musíte pojmenovat každou položku aplikace Excel, kterou chcete vyplnit požadovanými údaji.</span><span class="sxs-lookup"><span data-stu-id="93e44-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="93e44-637">Stáhněte si soubor [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) a uložte jej do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="93e44-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="93e44-638">Otevřete soubor v aplikaci Excel a zkontrolujte strukturu sešitu.</span><span class="sxs-lookup"><span data-stu-id="93e44-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="93e44-639">Jak ukazuje následující obrázek, stažená šablona byla navržena pro tisk specifických dotazníků, které představují otázky v dotazníku, spolu s příslušnými odpověďmi.</span><span class="sxs-lookup"><span data-stu-id="93e44-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Šablona Excel pro tisk zadaných dotazníků](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="93e44-641">Do této šablony byly přidány názvy z Excelu, aby se vyplnily podrobnosti dotazníku.</span><span class="sxs-lookup"><span data-stu-id="93e44-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="93e44-642">Pomocí Správce jmen můžete zkontrolovat názvy z Excelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-642">You can use Name Manager to review the Excel names.</span></span>

![Pomocí Správce jmen můžete zkontrolovat názvy z Excelu v dodané šabloně Excel](./media/er-quick-start1-template-names.png)

<span data-ttu-id="93e44-644">Štítky přehledů byly přidány jako pevný text v anglickém jazyce.</span><span class="sxs-lookup"><span data-stu-id="93e44-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="93e44-645">Štítky výkazů můžete nahradit novými názvy z aplikace Excel, které vyplní štítky textem závislým na jazyce pomocí [štítků](#AddMmLabels) formátu ER, jako jste to udělali pro výrazy závislé na jazyce v konfigurovaném mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="93e44-646">V tomto případě musí být štítky ER přidány v upravitelném formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="93e44-647">Jak ukazuje následující obrázek, byla určena záhlaví vlastní sestavy, aby aplikace Excel mohla stránkovat.</span><span class="sxs-lookup"><span data-stu-id="93e44-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Vlastní záhlaví sestavy v poskytnuté šabloně Excel](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="93e44-649">Návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-649">Design a format</span></span>

<span data-ttu-id="93e44-650">Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte vytvořit novou konfiguraci ER, která obsahuje komponent [formát](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="93e44-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="93e44-651">Komponent formátu musíte nakonfigurovat, abyste určili, jak bude šablona výkazu vyplněna požadovanými daty za běhu.</span><span class="sxs-lookup"><span data-stu-id="93e44-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="93e44-652">Dokončením kroků v části [Import navrženého formátu konfigurace](#FormatImport) můžete importovat požadovaný formát z poskytnutého souboru XML.</span><span class="sxs-lookup"><span data-stu-id="93e44-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="93e44-653">Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace formátu](#FormatCreate), chcete-li navrhnout tento formát od začátku.</span><span class="sxs-lookup"><span data-stu-id="93e44-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="93e44-654">Import navrženého formátu konfigurace</span><span class="sxs-lookup"><span data-stu-id="93e44-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="93e44-655">Stáhněte si soubor [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) a uložte jej do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="93e44-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="93e44-656">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="93e44-657">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="93e44-658">V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="93e44-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="93e44-659">Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="93e44-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="93e44-660">Kliknutím na tlačítko **OK** importujte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="93e44-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="93e44-661">Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace formátu](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="93e44-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="93e44-662">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="93e44-663">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-664">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="93e44-665">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="93e44-666">V rozevíracím dialogovém okně proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="93e44-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-667">V poli **Nový** vyberte **Formát založený na datovém modelu pro dotazníky**'.</span><span class="sxs-lookup"><span data-stu-id="93e44-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="93e44-668">Do pole **Název** zadejte **Setava dotazníku**'.</span><span class="sxs-lookup"><span data-stu-id="93e44-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="93e44-669">V poli **Verze datového modelu** vyberte **1**.</span><span class="sxs-lookup"><span data-stu-id="93e44-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="93e44-670">Pokud vyberete konkrétní verzi základního datového modelu, zobrazí se vám struktura odpovídající verze datového modelu jako struktura zdroje dat **Modelu** ve formátu, který je vytvořen.</span><span class="sxs-lookup"><span data-stu-id="93e44-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="93e44-671">Toto pole můžete ponechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="93e44-671">You can leave this field blank.</span></span> <span data-ttu-id="93e44-672">V takovém případě struktura verze **Návrh** datového modelu vám bude zobrazena jako struktura zdroje dat **Modelu** ve formátu, který je vytvořen.</span><span class="sxs-lookup"><span data-stu-id="93e44-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="93e44-673">Poté můžete svůj model upravit a změny okamžitě zobrazit ve svém formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="93e44-674">Tento přístup může zlepšit účinnost návrhu řešení ER když konfigurujete svůj datový model, mapování modelu a formátování současně.</span><span class="sxs-lookup"><span data-stu-id="93e44-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="93e44-675">Pokud vyberete konkrétní verzi základního datového modelu, můžete přepnout na **Návrh** verzi později, když začnete upravovat formát.</span><span class="sxs-lookup"><span data-stu-id="93e44-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="93e44-676">V poli **Definice datového modelu** vyberte definici **Kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="93e44-677">Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="93e44-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="93e44-678">Import šablony sestavy</span><span class="sxs-lookup"><span data-stu-id="93e44-678">Import a report template</span></span>

1. <span data-ttu-id="93e44-679">Na stránce **Konfigurace** vyberte v konfiguračním stromu **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="93e44-680">Vyberte **Návrhář** pro zahájení konfigurace vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="93e44-681">Na stránce **Návrhář formátu** v podokně akcí vyberte **Importovat** \> **Importovat z Excelu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="93e44-682">V dialogovém okně proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="93e44-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-683">Vyberte **Přidat šablonu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="93e44-684">Vyhledejte a vyberte místně uložený soubor **Questionnaires report template.xslx** a vyberte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="93e44-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="93e44-685">Kliknutím na tlačítko **OK** importujte šablonu.</span><span class="sxs-lookup"><span data-stu-id="93e44-685">Select **OK** to import the template.</span></span>

    ![Import šablony sestavy](./media/er-quick-start1-template-import.png)

<span data-ttu-id="93e44-687">**Excel\\Soubor** prvek formátu je automaticky přidán do upravitelného formátu jako kořenový element.</span><span class="sxs-lookup"><span data-stu-id="93e44-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="93e44-688">Navíc buď **Excel\\Rozsah** prvek formátu nebo **Excel\\Buňka** element formátu je automaticky přidán pro každý rozpoznaný Excelový název importované šablony.</span><span class="sxs-lookup"><span data-stu-id="93e44-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="93e44-689">**Excel\\Záhlaví** formát, který má vnořený **Řetězcový** prvek je automaticky přidán, aby odrážel nastavení záhlaví importované šablony.</span><span class="sxs-lookup"><span data-stu-id="93e44-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Struktura formátu, která zahrnuje automaticky přidané prvky v návrháři operace ER](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="93e44-691">Konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-691">Configure a format</span></span>

1. <span data-ttu-id="93e44-692">Na stránce **Návrhář formátů**, ve stromové struktuře, vyberte **Excel** kořenový prvek.</span><span class="sxs-lookup"><span data-stu-id="93e44-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="93e44-693">V kartě **Formát** na pravé straně stránky v poli **Název** zadejte <a name="AddFormatRootElement"></a>**Sestava**.</span><span class="sxs-lookup"><span data-stu-id="93e44-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="93e44-694">V poli **Jazykové předvolba** vyberte **Uživatelské předvolby** ke spuštění sestavy v preferovaném jazyce uživatele.</span><span class="sxs-lookup"><span data-stu-id="93e44-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="93e44-695">V poli **Předvolby jazykové verze** vyberte **Uživatelské předvolby** ke spuštění sestavy v preferované jazykové verzi uživatele.</span><span class="sxs-lookup"><span data-stu-id="93e44-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="93e44-696">Informace o tom, jak určit jazykové a kulturní kontexty pro proces ER, viz [Návrh vícejazyčných sestav](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Konfigurace nastavení jazyka a kultury pro navrženou sestavu v návrháři operace ER](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="93e44-698">Ve stromu formátu rozbalte kořenový uzel a poté vyberte **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="93e44-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="93e44-699">Na kartě **Formát**, pole **Směr replikace**, vyberte **Žádná replikace**, protože neočekáváte, že pro jeden dotazník budete mít více skupin výsledků.</span><span class="sxs-lookup"><span data-stu-id="93e44-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Definování směru replikace pro prvky formátu Oblast v návrháři operací ER](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="93e44-701">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="93e44-702">Definice datové vazby pro název sestavy</span><span class="sxs-lookup"><span data-stu-id="93e44-702">Define the data binding for a report title</span></span>

<span data-ttu-id="93e44-703">Musíte zadat datovou vazbu pro prvek formátu, který se používá k vyplnění názvu generované sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="93e44-704">Na stránce **Návrhář formátu** na kartě **Mapování** napravo, vyberte ve stromu formátu prvek **Sestavení\\ReportTile**.</span><span class="sxs-lookup"><span data-stu-id="93e44-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="93e44-705">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="93e44-706">V editoru vzorců vyberte **Přeložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="93e44-707">V dialogovém okně **Překlad textu** proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="93e44-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="93e44-708">Do pole **ID popisku** zadejte **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="93e44-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="93e44-709">Do pole **Text ve výchozím jazyce** zadejte **Sestava dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="93e44-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="93e44-710">Vyberte **Přeložit** a potom **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="93e44-711">Vyberte **Přeložit** pro zavření dialogového okna **Překlad textu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="93e44-712">Zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-712">Close the formula editor.</span></span>

    ![Konfigurace vazby k vyplnění názvu generované sestavy](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="93e44-714">Tuto techniku můžete použít k tomu, aby všechny ostatní štítky aktuální šablony byly závislé na jazyce.</span><span class="sxs-lookup"><span data-stu-id="93e44-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="93e44-715">Informace o tom, jak mohou být přidané štítky jedné konfigurace ER přeloženy do všech podporovaných jazyků, viz [Návrh vícejazyčných sestav](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="93e44-716">Kontrola zdrojových data modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-716">Review model data source</span></span>

1. <span data-ttu-id="93e44-717">Na stránce **Návrhář formátů**, na kartě **Mapování** vyberte záložku <a name="ModelDSName"></a>**model** zdrojových dat, který představuje základní datový model tohoto formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="93e44-718">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-718">Select **Edit**.</span></span>
3. <span data-ttu-id="93e44-719">Přečtěte si informace v dialogovém okně **Vlastnosti zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="93e44-720">Tento zdroj dat představuje verzi 1 **Dotazníkového** komponentu datového modelu, který je umístěný v **Model dotazníků** ER konfigurace.</span><span class="sxs-lookup"><span data-stu-id="93e44-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Vlastnosti modelu zdroje dat v návrháři operací ER](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="93e44-722">Vázání prvků formátu na pole zdroje dat</span><span class="sxs-lookup"><span data-stu-id="93e44-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="93e44-723">Chcete-li určit, jak je šablona vyplněna za běhu, musíte svázat každý prvek formátu, který je spojen s příslušným názvem Excelu, s jediným polem zdroje dat tohoto formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="93e44-724">Na stránce **Návrhář formátů**, ve stromové struktuře, vyberte **Sestava\\CompanyName** prvek formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="93e44-725">Na záložce **Mapování** vyberte **model.CompanyName** pole zdroje dat typu **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="93e44-726">Vyberte **Svázat** k zadání názvu společnosti do šablony.</span><span class="sxs-lookup"><span data-stu-id="93e44-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="93e44-727">Ve stromu formátů vyberte prvek **Sestava\\Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="93e44-728">Na záložce **Mapování** vyberte **model.Questionnaire** pole zdroje dat typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="93e44-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="93e44-729">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="93e44-729">Select **Bind**.</span></span>
7. <span data-ttu-id="93e44-730">Výběrem **Ukázat podrobnosti** zobrazíte další podrobnosti o prvcích formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="93e44-731">Prvek formátu rozsahu **Dotazník** je nakonfigurován jako vertikálně replikovaný.</span><span class="sxs-lookup"><span data-stu-id="93e44-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="93e44-732">Když je vázán na zdroj dat typu **Seznam záznamů**, vhodný **Dotazník** rozsahu šablony Excel se opakuje pro každý záznam vázaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Vazba prvku formátu dotazníku na příslušný zdroj dat seznamu záznamů v návrháři operací ER](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="93e44-734">Protože rozsah **Dotazník** šablony Excel je definován mezi řádky 5 až 14, tyto řádky se opakují pro každý vykazovaný dotazník.</span><span class="sxs-lookup"><span data-stu-id="93e44-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Řádky v šabloně Excel, které se budou opakovat ve vygenerované sestavě pro každý záznam ze zdrojů dat seznamu záznamů](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="93e44-736">Nakonfigurujte podobné vazby pro zbývající prvky formátu, jak je popsáno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="93e44-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="93e44-737">V této tabulce se předpokládá, že informace obsažené ve sloupci "Cesta ke zdroji dat" jsou pravdivé pouze při zapnuté funkci [relativní cesta](relative-path-data-bindings-er-models-format.md) ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="93e44-738">Formát cesty prvku</span><span class="sxs-lookup"><span data-stu-id="93e44-738">Format element path</span></span>                                      | <span data-ttu-id="93e44-739">Cesta ke zdroji dat</span><span class="sxs-lookup"><span data-stu-id="93e44-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="93e44-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="93e44-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="93e44-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="93e44-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="93e44-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="93e44-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="93e44-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="93e44-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="93e44-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="93e44-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="93e44-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="93e44-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="93e44-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="93e44-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="93e44-747">**\@.Active**, kde **\@** je **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="93e44-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="93e44-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="93e44-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="93e44-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="93e44-749">**\@.Code**</span></span> |
    | <span data-ttu-id="93e44-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="93e44-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="93e44-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="93e44-751">**\@.Description**</span></span> |
    | <span data-ttu-id="93e44-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="93e44-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="93e44-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="93e44-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="93e44-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="93e44-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="93e44-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="93e44-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="93e44-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="93e44-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="93e44-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="93e44-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="93e44-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="93e44-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="93e44-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="93e44-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="93e44-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="93e44-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="93e44-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="93e44-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="93e44-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="93e44-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="93e44-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="93e44-763">**\@.Question**</span></span> |
    | <span data-ttu-id="93e44-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="93e44-765">**\@.CollectionSequenceNumber**, kde **\@** je **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="93e44-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="93e44-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="93e44-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="93e44-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="93e44-767">**\@.Id**</span></span> |
    | <span data-ttu-id="93e44-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="93e44-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="93e44-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="93e44-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="93e44-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="93e44-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="93e44-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="93e44-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="93e44-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="93e44-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="93e44-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="93e44-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="93e44-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="93e44-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="93e44-775">**\@.Text**</span></span> |
    | <span data-ttu-id="93e44-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="93e44-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="93e44-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="93e44-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="93e44-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="93e44-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="93e44-779">**\@.CorrectAnswer**, kde **\@** je **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="93e44-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="93e44-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="93e44-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="93e44-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="93e44-781">**\@.Points**</span></span> |
    | <span data-ttu-id="93e44-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="93e44-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="93e44-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="93e44-783">**\@.Text**</span></span> |

9. <span data-ttu-id="93e44-784">Po dokončení zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="93e44-785">Následující obrázek ukazuje konečný stav mapování konfigurovaných datových vazeb na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigurované datové vazby v návrháři operace ER](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="93e44-787">Celá sbírka specifikovaných zdrojů dat a vazeb představuje komponentu mapování formátu konfigurovaného formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="93e44-788">Toto mapování formátu je zavoláno při spuštění konfigurovaného formátu pro generování sestav.</span><span class="sxs-lookup"><span data-stu-id="93e44-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="93e44-789">Spuštění navrženého formátu z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-789">Run a designed format from ER</span></span>

<span data-ttu-id="93e44-790">Nyní můžete spustit navržený formát pro účely testování ze stránky **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="93e44-791">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-792">Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="93e44-793">Vyberte **Návrhář** pro verzi formátu, která má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="93e44-794">Na stránce **Návrhář formátu** zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="93e44-795">V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="93e44-796">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="93e44-797">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="93e44-798">Prohlédněte si generovanou sestavu.</span><span class="sxs-lookup"><span data-stu-id="93e44-798">Review the generated report.</span></span>

<span data-ttu-id="93e44-799">Ve [výchozím nastavení](electronic-reporting-destinations.md#default-behavior) se vygenerovaná zpráva doručí jako soubor Excelu, který si můžete stáhnout.</span><span class="sxs-lookup"><span data-stu-id="93e44-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="93e44-800">Následující obrázky ukazují dvě stránky generované zprávy ve formátu Excel.</span><span class="sxs-lookup"><span data-stu-id="93e44-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Příklad vygenerované sestavy ve formátu Excel, strana 1](./media/er-quick-start1-report1a.png)

![Příklad vygenerované sestavy ve formátu Excel, strana 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="93e44-803">Vylaďte navržený formát</span><span class="sxs-lookup"><span data-stu-id="93e44-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="93e44-804">Upravte formát a změňte název generovaného dokumentu</span><span class="sxs-lookup"><span data-stu-id="93e44-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="93e44-805">Ve výchozím nastavení je vygenerovaný dokument pojmenován pomocí aliasu aktuálního uživatele.</span><span class="sxs-lookup"><span data-stu-id="93e44-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="93e44-806">Úpravou formátu můžete toto chování změnit tak, aby byl vygenerovaný dokument pojmenován na základě vlastní logiky.</span><span class="sxs-lookup"><span data-stu-id="93e44-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="93e44-807">Název vygenerovaného dokumentu může být například založen na aktuálním datu a času relace nebo na názvu sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="93e44-808">Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.</span><span class="sxs-lookup"><span data-stu-id="93e44-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="93e44-809">Na kartě **Mapování** vyberte **Upravit název souboru**.</span><span class="sxs-lookup"><span data-stu-id="93e44-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="93e44-810">Do pole **Vzorec** zadejte **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="93e44-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="93e44-811">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="93e44-812">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="93e44-813">Upravte formát a změňte pořadí otázek</span><span class="sxs-lookup"><span data-stu-id="93e44-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="93e44-814">Ve vygenerované sestavě nejsou otázky správně uspořádány.</span><span class="sxs-lookup"><span data-stu-id="93e44-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="93e44-815">Pořadí můžete změnit úpravou formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="93e44-816">Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.</span><span class="sxs-lookup"><span data-stu-id="93e44-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="93e44-817">Na kartě **Mapování** ve stromu formátu rozbalte **Sestava\\Dotazník\\Otázka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Prvek formátu otázek typu typu oblast v návrhář operací ER](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="93e44-819">Na kartě **Mapování** vyberte **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="93e44-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="93e44-820">Vyberte **Přidat** \> **Funkce\\Vypočítané pole** a pak v poli **Název** zadejte **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="93e44-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="93e44-821">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="93e44-822">V editoru vzorců do pole **Vzorec** zadejte **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** pro uspořádání seznamu otázek aktuálního dotazníku podle pořadového čísla.</span><span class="sxs-lookup"><span data-stu-id="93e44-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="93e44-823">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="93e44-824">Vyberte **OK** pro dokončení zadání nového vypočítaného pole.</span><span class="sxs-lookup"><span data-stu-id="93e44-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="93e44-825">Na kartě **Mapování** vyberte **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="93e44-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="93e44-826">Ve stromu formátu vyberte **Excel\\Dotazník\\Otázka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="93e44-827">Vyberte **Svázat** a poté potvrďte, že aktuální **model.Questionnaire.Questions** cesta je nahrazena novou **model.Questionnaire.OrderedQuestions** cestou ve všech vazbách vnořených prvků.</span><span class="sxs-lookup"><span data-stu-id="93e44-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="93e44-828">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-828">Select **Save**.</span></span>

![Vazba prvku formátu Otázka na konfigurovaný zdroj dat OrderedQuestions v Návrháři operací ER](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="93e44-830">Spuštění upraveného formátu z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-830">Run a modified format from ER</span></span>

<span data-ttu-id="93e44-831">Nyní můžete spouštět upravený formát pro účely testování z rozhraní ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="93e44-832">Na stránce **Návrhář formátu** zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="93e44-833">V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="93e44-834">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="93e44-835">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="93e44-836">Prohlédněte si generovanou sestavu.</span><span class="sxs-lookup"><span data-stu-id="93e44-836">Review the generated report.</span></span>

<span data-ttu-id="93e44-837">Následující obrázek ukazuje vygenerovanou sestavu ve formátu Excel, kde jsou otázky správně uspořádány.</span><span class="sxs-lookup"><span data-stu-id="93e44-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Generovaná sestava ve formátu Excel, která má správně uspořádané otázky](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="93e44-839">Dokončete návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-839">Complete the format design</span></span>

1. <span data-ttu-id="93e44-840">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-841">Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="93e44-842">Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="93e44-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="93e44-843">Vyberte **Změnit stav** \> **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="93e44-844">Stav verze 1.1 této konfigurace se změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="93e44-845">Verzi 1.1 již nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="93e44-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="93e44-846">Tato verze obsahuje nakonfigurovaný formát a lze ji použít k vytištění vlastní sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="93e44-847">Verze 1.2 této konfigurace je vytvořena a má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="93e44-848">Tuto verzi můžete upravit a tak upravit formát vašeho sestavení **Dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Verze konfigurovatelné konfigurace ER na stránce Konfigurace](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="93e44-850">Konfigurovaný formát je váš návrh sestavení **Dotazníku** a neobsahuje žádné vztahy k artefaktům specifickým pro Finance.</span><span class="sxs-lookup"><span data-stu-id="93e44-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="93e44-851">Vytvořte artefakty aplikace a pojmenujte navrženou sestavu</span><span class="sxs-lookup"><span data-stu-id="93e44-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="93e44-852">Jako uživatel v roli správce systému musíte vyvinout novou logiku, aby nakonfigurovaný formát ER mohl být vyvolán z uživatelského rozhraní aplikace (UI) pro vygenerování vaší vlastní sestavy.</span><span class="sxs-lookup"><span data-stu-id="93e44-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="93e44-853">V současné době ER nenabízí žádné možnosti pro konfiguraci tohoto typu logiky.</span><span class="sxs-lookup"><span data-stu-id="93e44-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="93e44-854">Proto je nutné provést určité inženýrské práce.</span><span class="sxs-lookup"><span data-stu-id="93e44-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="93e44-855">Pro vyvinutí nové logiky je nutné nasadit topologii, která podporuje průběžné sestavování.</span><span class="sxs-lookup"><span data-stu-id="93e44-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="93e44-856">Další informace naleznete v tématu [Nasazení topologií, které podporují automatizaci průběžného sestavení a testů](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="93e44-857">Také musí mít přístup k vývojovému prostředí pro tuto topologii.</span><span class="sxs-lookup"><span data-stu-id="93e44-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="93e44-858">Další informace o dostupných ER API najdete v tématu [API rozhraní architektury elektronického výkaznictví](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="93e44-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="93e44-859">Úprava zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="93e44-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="93e44-860">Přidejte třídu datového kontraktu</span><span class="sxs-lookup"><span data-stu-id="93e44-860">Add a data contract class</span></span>

<span data-ttu-id="93e44-861">Přidejte nový **DotazníkyErReportContract** třídu do Microsoft Visual Studio projektu a napište kód, který specifikuje datový kontrakt, který by měl být použit pro spuštění nakonfigurovaného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="93e44-862">Přidejte třídu tvůrce uživatelského rozhraní</span><span class="sxs-lookup"><span data-stu-id="93e44-862">Add a UI builder class</span></span>

<span data-ttu-id="93e44-863">Přidejte novou **DotazníkyReportUIBuilder** třídu do Visual Studio projektu a napiště kód pro vygenerování dialogového okna runtime, které bude použito k vyhledání ID mapování formátu formátu ER, který musí být spuštěn.</span><span class="sxs-lookup"><span data-stu-id="93e44-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="93e44-864">Poskytovaný kód vyhledá pouze formáty ER, které obsahují zdroj dat typu **Datový model**, který odkazuje na datový model **[Dotazníky](#DataModeName)** pomocí **[Kořenové](#RootDefinitionName)** definice.</span><span class="sxs-lookup"><span data-stu-id="93e44-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="93e44-865">Alternativně můžete použít body integrace ER k filtrování formátů ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="93e44-866">Další informace viz [API pro zobrazení vyhledávání mapování formátu](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="93e44-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="93e44-867">Přidejte třídu poskyovatele dat</span><span class="sxs-lookup"><span data-stu-id="93e44-867">Add a data provider class</span></span>

<span data-ttu-id="93e44-868">Přidejte nový **QuestionnairesErReportDP** třídu do Visual Studio projektu a napište kód, který uvádí poskytovatele dat, který by měl být použit pro spuštění nakonfigurovaného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="93e44-869">Poskytnutý kód zahrnuje pouze datový kontrakt pro tohoto poskytovatele dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="93e44-870">Přidejte soubor štítků</span><span class="sxs-lookup"><span data-stu-id="93e44-870">Add a labels file</span></span>

<span data-ttu-id="93e44-871">Přidejte nový **QuestionnairesErReportLabels\_en-US** soubor štítků do vašeho Visual Studio projektu a určete následující štítky pro nové prostředky uživatelského rozhraní:</span><span class="sxs-lookup"><span data-stu-id="93e44-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="93e44-872">**\@QuestionnairesReport** štítek pro novou položku nabídky, která obsahuje následující text v americké angličtině (en-US): **Sestava dotazníků (využívá ER)**</span><span class="sxs-lookup"><span data-stu-id="93e44-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="93e44-873">**\@QuestionnairesReportBatchJobDescription** štítek pro název dávkové úlohy, pokud bure vybraný formát ER spuštěn jako dávková úloha</span><span class="sxs-lookup"><span data-stu-id="93e44-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="93e44-874">Přidejte třídu služby sestav</span><span class="sxs-lookup"><span data-stu-id="93e44-874">Add a report service class</span></span>

<span data-ttu-id="93e44-875">Přidejte novou **QuestionnairesErReportService** třídu do vašeho Visual Studio projektu a napište kód, který volá formát ER, identifikuje jej pomocí ID mapování formátu a jako parametr poskytuje datový kontrakt.</span><span class="sxs-lookup"><span data-stu-id="93e44-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="93e44-876">Když musíte použít formát ER, který spouští aplikační data, musíte nakonfigurovat zdroj dat typu **Datový model** v mapování formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="93e44-877">Tento zdroj dat odkazuje na konkrétní část specifikovaného datového modelu pomocí jediné kořenové definice.</span><span class="sxs-lookup"><span data-stu-id="93e44-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="93e44-878">Při spuštění formátu ER tento zdroj dat žádá o přístup k příslušnému mapování modelu ER, které je nakonfigurováno pro daný model a definici kořenů.</span><span class="sxs-lookup"><span data-stu-id="93e44-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="93e44-879">Všechny informace, které byste mohli připravit ve zdrojovém kódu a uložit jako součást datového kontraktu, lze předat do běžícího formátu ER pomocí mapování modelu ER tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="93e44-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="93e44-880">V mapování modelu ER musíte nakonfigurovat zdroj dat typu **Objekt**, který odkazuje na třídu **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="93e44-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="93e44-881">Chcete-li identifikovat mapování modelu, musíte určit zdroj dat, který toto mapování modelu volá.</span><span class="sxs-lookup"><span data-stu-id="93e44-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="93e44-882">V zadaném kódu je tento zdroj dat specifikován konstantou **ERModelDataSourceName**, která má hodnotu **[model](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="93e44-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="93e44-883">Chcete-li identifikovat, který zdroj dat se používá k vystavení datového kontraktu v mapování modelu, musíte zadat název zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="93e44-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="93e44-884">V zadaném kódu je tento název specifikován konstantou **ParametersDataSourceName**, která má hodnotu <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="93e44-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="93e44-885">V novém prostředí budete možná muset aktualizovat metadata ER, aby byl tento typ třídy k dispozici v návrháři mapování modelů ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="93e44-886">Další informace získáte v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="93e44-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="93e44-887">Přidejte třídu kontrolera sestav</span><span class="sxs-lookup"><span data-stu-id="93e44-887">Add a report controller class</span></span>

<span data-ttu-id="93e44-888">Přidejte novou třídu **QuestionnairesErReportController** do vašeho Visual Studio projektu a napiště kód, který spouští formát ER v synchronním režimu nebo dávkovém režimu v dialogovém okně, které je vytvořeno na základě logiky poskytované třídou **QuestionnairesErReportUIBuilder**.</span><span class="sxs-lookup"><span data-stu-id="93e44-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="93e44-889">Přidejte položku nabídky</span><span class="sxs-lookup"><span data-stu-id="93e44-889">Add a menu item</span></span>

<span data-ttu-id="93e44-890">Přidejte novou **QuestionnairesErReport** položku nabídky do Visual Studio projektu.</span><span class="sxs-lookup"><span data-stu-id="93e44-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="93e44-891">Ve vlastnosti **Objekt** tato položka nabídky odkazuje na třídu **QuestionnairesErReportController** a používá se k určení uživatelského oprávnění k výběru a spuštění formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="93e44-892">Ve vlastnosti **Označení** tato položka nabídky odkazuje na štítek **\@QuestionnairesReport**, který jste vytvořili dříve, aby v uživatelském rozhraní aplikace byl uveden správný text.</span><span class="sxs-lookup"><span data-stu-id="93e44-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="93e44-893">Přidejte položku nabídky k nabídce</span><span class="sxs-lookup"><span data-stu-id="93e44-893">Add a menu item to a menu</span></span>

<span data-ttu-id="93e44-894">Přidejte existující **KM** menu do vašeho Visual Studio projektu.</span><span class="sxs-lookup"><span data-stu-id="93e44-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="93e44-895">Musíte přidat novou položku **QuestionnairesErReport** typu **Výstup** do této nabídky.</span><span class="sxs-lookup"><span data-stu-id="93e44-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="93e44-896">Tato položka musí odkazovat na **QuestionnairesErReport** položku nabídky, která je popsána v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="93e44-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="93e44-897">Sestavte Visual Studio projekt</span><span class="sxs-lookup"><span data-stu-id="93e44-897">Build a Visual Studio project</span></span>

<span data-ttu-id="93e44-898">Vytvořte svůj projekt a zpřístupněte uživatelům novou položku nabídky.</span><span class="sxs-lookup"><span data-stu-id="93e44-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="93e44-899">Spusťte formát z aplikace</span><span class="sxs-lookup"><span data-stu-id="93e44-899">Run a format from the application</span></span>

1. <span data-ttu-id="93e44-900">Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.</span><span class="sxs-lookup"><span data-stu-id="93e44-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Výběrem položky nabídky Přehled dotazníků (využívá ER) v modulu Dotazník spustíte nakonfigurovaní ER formát](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="93e44-902">V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="93e44-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="93e44-903">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-903">Select **OK**.</span></span>
4. <span data-ttu-id="93e44-904">V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="93e44-905">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="93e44-906">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-906">Select **OK** to run the report.</span></span>

    ![Zadání kritérií výběru v dialogovém okně Elektronický výkaz](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="93e44-908">Prohlédněte si generovanou sestavu.</span><span class="sxs-lookup"><span data-stu-id="93e44-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="93e44-909">Vylaďte navržené řešení ER</span><span class="sxs-lookup"><span data-stu-id="93e44-909">Tune a designed ER solution</span></span>

<span data-ttu-id="93e44-910">Konfigurované řešení ER můžete upravit tak, že používá třídu poskytovatele dat, kterou jste vyvinuli, pro přístup k podrobnostem o běžícím formátu ER a tak, že do vygenerovaného výkazu zadá název tohoto formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="93e44-911">Úprava mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="93e44-912">Přidání zdroje dat pro přístup k objektu kontraktu dat</span><span class="sxs-lookup"><span data-stu-id="93e44-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="93e44-913">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-914">Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Mapování dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="93e44-915">Vyberte **Návrhář** k otevření stránky **Mapování modelu k datovým zdrojům**.</span><span class="sxs-lookup"><span data-stu-id="93e44-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="93e44-916">Vyberte **Návrhář** k otevření vybraného mapování v návrháři mapových modelů.</span><span class="sxs-lookup"><span data-stu-id="93e44-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="93e44-917">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Objekt**.</span><span class="sxs-lookup"><span data-stu-id="93e44-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="93e44-918">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="93e44-919">V dialogovém okně, v poli **Název**, zadejte **[RunTimeParameters](#DataContractDSName)**, jak je definováno ve zdrojovém kódu třídy **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="93e44-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="93e44-920">Do pole **Třída** zadejte **[QuestionnairesErReportContract](#DataContractClass)**, naprogramovaný dříve.</span><span class="sxs-lookup"><span data-stu-id="93e44-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="93e44-921">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-921">Select **OK**.</span></span>
10. <span data-ttu-id="93e44-922">Rozšiřte **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="93e44-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="93e44-923">Přidaný zdroj dat poskytuje informace o ID záznamu běžícího mapování formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Přidán zdroj dat v návrháři mapování modelů ER](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="93e44-925">Přidejte zdroj dat pro přístup k záznamům mapování formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="93e44-926">Pokračujte v úpravách mapování vybraného modelu přidáním zdroje dat pro přístup k záznamům mapování formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="93e44-927">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="93e44-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="93e44-928">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="93e44-929">V dialogovém okně do pole **Název** zadejte **ER1**.</span><span class="sxs-lookup"><span data-stu-id="93e44-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="93e44-930">Do pole **Tabulka** zadejte **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="93e44-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="93e44-931">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="93e44-932">Přidejte zdroj dat pro přístup k záznam mapování běžícího formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="93e44-933">Pokračujte v úpravách mapování vybraného modelu přidáním zdroje dat pro přístup k záznamům mapování formátu běžícího ER formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="93e44-934">Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Funkce\\Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="93e44-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="93e44-935">V podokně **Zdroje dat** vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="93e44-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="93e44-936">V dialogovém okně do pole **Název** zadejte **ER2**.</span><span class="sxs-lookup"><span data-stu-id="93e44-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="93e44-937">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="93e44-938">V editoru vzorců do pole **Vzorec** zadejte **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="93e44-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="93e44-939">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="93e44-940">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="93e44-941">Zadejte název datového modelu běžícího formátu ER</span><span class="sxs-lookup"><span data-stu-id="93e44-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="93e44-942">Pokračujte v úpravách mapování vybraného modelu tak, aby se do datového modelu zadal název běžícího formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="93e44-943">Na stránce **Návrhář mapování modelu** v podokně **Datový model** otevřete **ExecutionContext** a poté zvolte **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="93e44-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="93e44-944">V podokně **Datový model** vyberte **Upravit** pro konfiguraci vazby dat pro pole vybraného datového modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="93e44-945">V editoru vzorců do pole **Vzorec** zadejte **FIRSTORNULL (ER2.'\>Relations.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="93e44-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="93e44-946">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="93e44-947">Protože jste použili **FormatName**, v konfigurovaném mapování modelu se nyní zobrazí název formátu ER, který během provádění volá toto mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Vazba pole datového modelu na metodu přidaného zdroje dat v návrháři mapování modelu ER](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="93e44-949">Dokončení návrhu mapování modelu</span><span class="sxs-lookup"><span data-stu-id="93e44-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="93e44-950">Na stránce **Návrhář mapování modelu** zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="93e44-951">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="93e44-951">Close the page.</span></span>
3. <span data-ttu-id="93e44-952">Zavřete stránku Mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="93e44-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="93e44-953">Na stránce **Konfigurace** ve stromu konfigurace zkontrolujte, zda je konfigurace **Mapování dotazníku** stále vybrána.</span><span class="sxs-lookup"><span data-stu-id="93e44-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="93e44-954">Poté na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="93e44-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="93e44-955">Vyberte **Změnit stav** \> **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="93e44-956">Stav verze 1.2 této konfigurace se změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="93e44-957">Verzi 1.2 již nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="93e44-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="93e44-958">Tato verze obsahuje konfigurovaný model mapování a lze ji použít jako základ pro další konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="93e44-959">Verze 1.3 této konfigurace je vytvořena a má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="93e44-960">Tuto verzi můžete upravit a tak upravit mapování modelu **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="93e44-961">Změna formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-961">Modify a format</span></span>

<span data-ttu-id="93e44-962">Konfigurovaný formát ER můžete upravit tak, aby jeho název byl zobrazen v zápatí sestavy, která je generována při spuštění formátu ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="93e44-963">Přidat nový prvek formátu.</span><span class="sxs-lookup"><span data-stu-id="93e44-963">Add a new format element</span></span>

1. <span data-ttu-id="93e44-964">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-965">Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="93e44-966">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="93e44-966">Select **Designer**.</span></span>
4. <span data-ttu-id="93e44-967">Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.</span><span class="sxs-lookup"><span data-stu-id="93e44-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="93e44-968">Vyberte **Přidat** pro přidání nového prveku vnořeného formátu pro vybranou kořenovou položku **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="93e44-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="93e44-969">Vyberte **Excel\\Zápatí**.</span><span class="sxs-lookup"><span data-stu-id="93e44-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="93e44-970">Do pole **Název** zadejte **Zápatí**.</span><span class="sxs-lookup"><span data-stu-id="93e44-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="93e44-971">Vyberte **Sestava\Zápatí** a pak vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="93e44-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="93e44-972">Vyberte **Text\\Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="93e44-973">Vázání přidaného prvku formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-973">Bind the added format element</span></span>

1. <span data-ttu-id="93e44-974">Na stránce **Návrhář formátu**, na kartě **Mapování**, pro aktivní prvek **Zápatí\\Řetězec**, vyberte **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="93e44-975">V editoru vzorců do pole **Vzorec** zadejte **CONCATENATE("\&C\&10 ", FORMAT(" Vygenerováno "\%1 'ER řešením', model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="93e44-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="93e44-976">Zvolte **Uložit** a pak zavřete editor vzorců.</span><span class="sxs-lookup"><span data-stu-id="93e44-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="93e44-977">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-977">Select **Save**.</span></span>

<span data-ttu-id="93e44-978">Konfigurovaný formát byl nyní upraven tak, aby jeho nýzev byl vložený do zápatí vygenerované sestavy pomocí prvku **Zápatí\\Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="93e44-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Přidání prvku formátu zápatí do konfigurovaného formátu v návrháři operací ER](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="93e44-980">Dokončete návrh formátu</span><span class="sxs-lookup"><span data-stu-id="93e44-980">Complete the format design</span></span>

1. <span data-ttu-id="93e44-981">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="93e44-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="93e44-982">Na stránce **Konfigurace** ve stromu konfigurace zkontrolujte, zda je konfigurace **Sestava dotazníku** stále vybrána.</span><span class="sxs-lookup"><span data-stu-id="93e44-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="93e44-983">Poté na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="93e44-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="93e44-984">Vyberte **Změnit stav** \> **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="93e44-985">Stav verze 1.2 této konfigurace se změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="93e44-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="93e44-986">Verzi 1.2 již nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="93e44-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="93e44-987">Tato verze obsahuje konfigurovaný formát a lze ji použít jako základ pro další konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="93e44-988">Verze 1.3 této konfigurace je vytvořena a má stav **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="93e44-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="93e44-989">Tuto verzi můžete upravit a tak upravit sestavení **Dotazník**.</span><span class="sxs-lookup"><span data-stu-id="93e44-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="93e44-990">Spusťte formát z aplikace</span><span class="sxs-lookup"><span data-stu-id="93e44-990">Run a format from the application</span></span>

1. <span data-ttu-id="93e44-991">Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.</span><span class="sxs-lookup"><span data-stu-id="93e44-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="93e44-992">V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="93e44-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="93e44-993">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-993">Select **OK**.</span></span>
4. <span data-ttu-id="93e44-994">V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="93e44-995">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="93e44-996">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="93e44-997">Zkontrolujte vygenerovaný soubor ve fromátu Excel.</span><span class="sxs-lookup"><span data-stu-id="93e44-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="93e44-998">Všimněte si, že zápatí generované sestavy obsahuje název formátu ER, který byl použit k jeho vygenerování.</span><span class="sxs-lookup"><span data-stu-id="93e44-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Vygenerovaný soubor ve formátu Excel](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="93e44-1000">Spusťte formát z ER</span><span class="sxs-lookup"><span data-stu-id="93e44-1000">Run a format from ER</span></span>

1. <span data-ttu-id="93e44-1001">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="93e44-1002">Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="93e44-1003">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="93e44-1004">V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="93e44-1005">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="93e44-1006">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="93e44-1007">Zkontrolujte vygenerovaný soubor ve fromátu Excel.</span><span class="sxs-lookup"><span data-stu-id="93e44-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="93e44-1008">Všimněte si, že zápatí generované sestavy neobsahuje název formátu ER, který byl použit k jeho vygenerování, protože objekt datového kontraktu nebyl předán do běžícího mapování modelu, když byl volán formátem ER, který byl spuštěn z ER.</span><span class="sxs-lookup"><span data-stu-id="93e44-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="93e44-1009">Konfigurace cílového formátu pro náhled na obrazovce</span><span class="sxs-lookup"><span data-stu-id="93e44-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="93e44-1010">Přejděte do nabídky **Správa organizace** \> **Elektronická sestava** \> **Místo určení elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="93e44-1011">Na stránce **Cíl elektronického výkaznictví** přidejte cílový záznam pro nakonfigurovaný Formát ER **Sestava dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="93e44-1012">Na pevné záložce **Cílové místo souboru**, nastavte **Obrazovka** [cíl](er-destination-type-screen.md) pro **Sestavení** formátovací komponent, který byl [přidán](#AddFormatRootElement) jako kořenový prvek nakonfigurovaného formátu ER **Sestavení dotazníku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="93e44-1013">Na pevné záložce **Nastavení převodu PDF**, nakonfigurujte cíl pro převod zprávy do [formátu PDF](electronic-reporting-destinations.md#OutputConversionToPDF) který používá orientaci stránky **na šířku**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Konfigurace vlastního cíle obrazovky pro formát ER na stránce Cíle elektronického hlášení](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="93e44-1015">Spusťte formát z aplikace a zobrazte jej jako dokument PDF</span><span class="sxs-lookup"><span data-stu-id="93e44-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="93e44-1016">Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="93e44-1017">V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="93e44-1018">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1018">Select **OK**.</span></span>
4. <span data-ttu-id="93e44-1019">V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="93e44-1020">Možnost filtrování potvrďte výběrem tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="93e44-1021">Na pevné záložce **Cíle** si všimněte, že pole **Výstup** je nastaveno na **Obrazovka**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="93e44-1022">Pokud chcete změnit nakonfigurovaný cíl, vyberte **Změna**.</span><span class="sxs-lookup"><span data-stu-id="93e44-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Dialogové okno hlášení ER runtime, kde můžete změnit nakonfigurovaný cíl](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="93e44-1024">Klepnutím na tlačítko **OK** sestavu spustíte.</span><span class="sxs-lookup"><span data-stu-id="93e44-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="93e44-1025">Zkontrolujte vygenerovaný soubor ve formátu Excel.</span><span class="sxs-lookup"><span data-stu-id="93e44-1025">Review the generated report in PDF format.</span></span>

    ![Náhled vygenerovaného souboru ve fromátu Excel.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="93e44-1027">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="93e44-1027">Additional resources</span></span>

- [<span data-ttu-id="93e44-1028">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="93e44-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="93e44-1029">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="93e44-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="93e44-1030">Návrh vícejazyčných sestav</span><span class="sxs-lookup"><span data-stu-id="93e44-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="93e44-1031">API rozhraní architektury elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="93e44-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="93e44-1032">Funkce CASE</span><span class="sxs-lookup"><span data-stu-id="93e44-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="93e44-1033">Funkce CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="93e44-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="93e44-1034">Funkce DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="93e44-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="93e44-1035">Funkce FILTER</span><span class="sxs-lookup"><span data-stu-id="93e44-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="93e44-1036">Funkce FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="93e44-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="93e44-1037">Funkce FORMAT</span><span class="sxs-lookup"><span data-stu-id="93e44-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="93e44-1038">Funkce IF</span><span class="sxs-lookup"><span data-stu-id="93e44-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="93e44-1039">Funkce ORDERBY</span><span class="sxs-lookup"><span data-stu-id="93e44-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="93e44-1040">Funkce SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="93e44-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]