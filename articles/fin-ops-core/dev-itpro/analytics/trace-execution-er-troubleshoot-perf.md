---
title: Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem
description: Toto téma obsahuje informace o způsobu použití funkce sledování výkonu v elektronickém výkaznictví pro řešení potíží s výkonem.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295566"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="0b7bd-103">Sledování provádění formátů elektronického výkaznictví za účelem řešení potíží s výkonem</span><span class="sxs-lookup"><span data-stu-id="0b7bd-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0b7bd-104">V rámci procesu navrhování konfigurací elektronického výkaznictví pro generování elektronických dokumentů definujete metodu, která se používá k získání dat z aplikace a jejich zadávání do generovaného výstupu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="0b7bd-105">Funkce sledování výkonu elektronického výkaznictví pomáhá významně snižovat čas a náklady, které jsou spojeny se shromažďováním podrobností o provedení formátu elektronického výkaznictví a jejich použití k řešení potíží s výkonem.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="0b7bd-106">Tento kurz poskytuje pokyny k interpretaci sledování výkonu pro provedené formáty elektronického výkaznictví a způsob použití informací z těchto sledování k vylepšení výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b7bd-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="0b7bd-107">Prerequisites</span></span>

<span data-ttu-id="0b7bd-108">Pro dokončení příkladů v tomto kurzu musíte mít následující přístup:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="0b7bd-109">Přejděte k některé z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="0b7bd-110">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="0b7bd-111">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0b7bd-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="0b7bd-112">System administrator</span></span>

- <span data-ttu-id="0b7bd-113">Přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako aplikace, pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="0b7bd-114">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="0b7bd-115">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0b7bd-116">Správce systému</span><span class="sxs-lookup"><span data-stu-id="0b7bd-116">System administrator</span></span>

<span data-ttu-id="0b7bd-117">Je také nutné stáhnout a lokálně uložit následující soubory.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="0b7bd-118">Soubor</span><span class="sxs-lookup"><span data-stu-id="0b7bd-118">File</span></span>                                  | <span data-ttu-id="0b7bd-119">Obsah</span><span class="sxs-lookup"><span data-stu-id="0b7bd-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="0b7bd-120">Model sledování výkonu - verze 1</span><span class="sxs-lookup"><span data-stu-id="0b7bd-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="0b7bd-121">Vzorová konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="0b7bd-122">Metadata sledování výkonu - verze 1</span><span class="sxs-lookup"><span data-stu-id="0b7bd-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="0b7bd-123">Vzorová konfigurace metadat elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="0b7bd-124">Mapování sledování výkonu - verze 1.1</span><span class="sxs-lookup"><span data-stu-id="0b7bd-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="0b7bd-125">Vzorová konfigurace mapování elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="0b7bd-126">Formát sledování výkonu - verze 1.1</span><span class="sxs-lookup"><span data-stu-id="0b7bd-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="0b7bd-127">Vzorová konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="0b7bd-128">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="0b7bd-128">Configure ER parameters</span></span>

<span data-ttu-id="0b7bd-129">Každé sledování výkonu elektronického výkaznictví, které je generováno v aplikaci, je uloženo jako příloha záznamu protokolu provádění.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="0b7bd-130">Pro správu těchto příloh se používá architektura správy dokumentů (DM).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="0b7bd-131">Parametry elektronického výkaznictví je nutné nakonfigurovat s předstihem, aby bylo možné určit typ dokumentu ve správě dokumentů, který se má použít pro připojení sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="0b7bd-132">V pracovním prostoru **Elektronické sestavy** vyberte **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="0b7bd-133">Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Stránka parametrů elektronického výkaznictví](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="0b7bd-135">Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):</span><span class="sxs-lookup"><span data-stu-id="0b7bd-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="0b7bd-136">**Třída:** Připojit soubor</span><span class="sxs-lookup"><span data-stu-id="0b7bd-136">**Class:** Attach file</span></span>
- <span data-ttu-id="0b7bd-137">**Skupina:** Soubor</span><span class="sxs-lookup"><span data-stu-id="0b7bd-137">**Group:** File</span></span>

![Stránka typu dokumentu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="0b7bd-139">Vybraný typ dokumentu musí být k dispozici ve všech společnostech aktuální instance, protože přílohy správy dokumentů jsou specifické pro konkrétní společnost.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="0b7bd-140">Konfigurace parametrů RCS</span><span class="sxs-lookup"><span data-stu-id="0b7bd-140">Configure RCS parameters</span></span>

<span data-ttu-id="0b7bd-141">Sledování výkonu elektronického výkaznictví, která jsou generována, budou importována do RCS pro analýzu pomocí návrháře formátu elektronického výkaznictví a návrháře mapování elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="0b7bd-142">Vzhledem k tomu, že sledování výkonu elektronického výkaznictví jsou uložena jako přílohy záznamu protokolu spouštění, který souvisí s formátem elektronického výkaznictví, je nutné předem nakonfigurovat parametry RCS, aby bylo možné určit typ dokumentu správy dokumentů, který se má použít pro připojení sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="0b7bd-143">V instanci RCS zřízené pro vaši společnost vyberte v pracovním prostoru **Elektronické výkaznictví** možnost **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="0b7bd-144">Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Stránka parametrů elektronického výkaznictví v RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="0b7bd-146">Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):</span><span class="sxs-lookup"><span data-stu-id="0b7bd-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="0b7bd-147">**Třída:** Připojit soubor</span><span class="sxs-lookup"><span data-stu-id="0b7bd-147">**Class:** Attach file</span></span>
- <span data-ttu-id="0b7bd-148">**Skupina:** Soubor</span><span class="sxs-lookup"><span data-stu-id="0b7bd-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="0b7bd-149">Návrh řešení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-149">Design an ER solution</span></span>

<span data-ttu-id="0b7bd-150">Předpokládejme, že jste začali navrhovat nové řešení elektronického výkaznictví pro generování nové sestavy, která představuje transakce dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="0b7bd-151">Momentálně můžete najít transakce pro zvoleného dodavatele na stránce **Transakce dodavatele** (přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé**, zvolte dodavatele a potom v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Transakce**).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="0b7bd-152">Chcete však mít všechny transakce dodavatele současně v jednom elektronickém dokumentu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="0b7bd-153">Toto řešení bude obsahovat několik konfigurací elektronického výkaznictví, které obsahují požadovaný datový model, metadata, mapování modelu a součásti formátu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="0b7bd-154">Přihlaste se k instanci RCS, která byla pro vaši společnost zřízena.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="0b7bd-155">V tomto kurzu vytvoříte a upravíte konfigurace pro vzorovou společnost **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="0b7bd-156">Proto se ujistěte, že tento poskytovatel konfigurace byl přidán do RCS a vybrán jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="0b7bd-157">Pokyny naleznete v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="0b7bd-158">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="0b7bd-159">Na stránce **Konfigurace** importujte konfigurace elektronického výkaznictví, které jste stáhli jako nezbytný požadavek do RCS, v následujícím pořadí: datový model, metadata, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="0b7bd-160">Pro každou konfiguraci postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="0b7bd-161">V podokně akcí vyberte **Exchange \> Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="0b7bd-162">Zvolte **Procházet** a vyberte příslušný soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="0b7bd-163">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-163">Select **OK**.</span></span>

    ![Stránka konfigurace v RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="0b7bd-165">Spuštění řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="0b7bd-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="0b7bd-166">Předpokládejme, že jste dokončili návrh první verze řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="0b7bd-167">Nyní ji chcete vyzkoušet ve své instanci a analyzovat výkon provedení.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="0b7bd-168">Import konfigurace elektronického výkaznictví z RCS do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0b7bd-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="0b7bd-169">Přihlaste se k instanci aplikace.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="0b7bd-170">V tomto kurzu naimportujete konfigurace z vaší instance RCS (kde navrhujete komponenty elektronického výkaznictví) do své instance (kde je otestujete a nakonec je použijete).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="0b7bd-171">Proto je nutné zajistit, aby byly připraveny všechny požadované artefakty.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="0b7bd-172">Další pokyny získáte v postupu [Import konfigurací elektronického výkaznictví ze služby RCS (Regulatory Configuration Services)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="0b7bd-173">Pomocí následujícího postupu importujte konfigurace z RCS do aplikace:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="0b7bd-174">V pracovním prostoru **Elektronické výkaznictví** na dlaždici pro poskytovatele konfigurace **Litware, Inc** . vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="0b7bd-175">Na stránce **Úložiště konfigurací** vyberte úložiště typu **RCS** a poté zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="0b7bd-176">Na záložce s náhledem **Konfigurace** vyberte konfiguraci **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="0b7bd-177">Na záložce s náhledem **Verze** zvolte verzi **1.1** zvolené konfigurace a poté zvolte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Stránka úložiště konfigurace](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="0b7bd-179">Odpovídající verze konfigurací datových modelů a mapování modelů jsou automaticky importovány jako předpoklady pro importovanou konfiguraci formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="0b7bd-180">Zapnutí sledování výkonu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="0b7bd-181">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="0b7bd-182">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0b7bd-183">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="0b7bd-184">V poli **Formát sledování provádění** upřesněte formát generovaného sledování výkonu, ve kterém by měly být uloženy podrobnosti o provádění pro formát elektronického výkaznictví a prvky mapování:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="0b7bd-185">**Ladit formát sledování** - Tuto hodnotu vyberte, pokud plánujete interaktivně spustit formát ER, který má krátkou dobu provedení.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="0b7bd-186">Poté se zahájí shromažďování podrobností o provádění formátu ER.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="0b7bd-187">Je-li vybrána tato hodnota, sledování výkonu shromažďuje informace o době strávené na následujících akcích:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="0b7bd-188">Spuštění každého zdroje dat v mapování modelu, které je voláno za účelem získání dat</span><span class="sxs-lookup"><span data-stu-id="0b7bd-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="0b7bd-189">Zpracování jednotlivých položek formátu za účelem zadání dat ve výstupu, který je generován</span><span class="sxs-lookup"><span data-stu-id="0b7bd-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="0b7bd-190">Pokud vyberete hodnotu **Ladit formát sledování**, můžete analyzovat obsah trasování v návrháři provozu ER.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="0b7bd-191">Zde si můžete prohlédnout formát ER nebo mapovací prvky, které jsou uvedeny v trasování.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="0b7bd-192">**Agregovaný formát sledování** - Tuto hodnotu vyberte, pokud plánujete pustit formát ER, který má dlouhou dobu provedení v dávkovém režimu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="0b7bd-193">Poté se zahájí shromažďování agregovaných podrobností o provádění formátu ER.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="0b7bd-194">Je-li vybrána tato hodnota, sledování výkonu shromažďuje informace o době strávené na následujících akcích:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="0b7bd-195">Spuštění každého zdroje dat v mapování modelu, které je voláno za účelem získání dat</span><span class="sxs-lookup"><span data-stu-id="0b7bd-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="0b7bd-196">Spuštění každého zdroje dat v mapování formátu, které je voláno za účelem získání dat</span><span class="sxs-lookup"><span data-stu-id="0b7bd-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="0b7bd-197">Zpracování jednotlivých položek formátu za účelem zadání dat ve výstupu, který je generován</span><span class="sxs-lookup"><span data-stu-id="0b7bd-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="0b7bd-198">Hodnota **Agregovaný formát trasování** je k dispozici v Microsoft Dynamics 365 Finance verze 10.0.20 a novější.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="0b7bd-199">V návrháři formátu ER a návrháři mapování modelů ER můžete zobrazit celkovou dobu provedení pro jednu komponentu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="0b7bd-200">Trasování dále obsahuje podrobnosti o spuštění, například počet spuštění a minimální a maximální čas jednoho provedení.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="0b7bd-201">Toto trasování je shromažďováno na základě cesty trasovaných komponent.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="0b7bd-202">Statistiky proto mohou být nesprávné, pokud jedna nadřazená komponenta obsahuje několik nepojmenovaných podřízených komponent nebo když má několik podřízených komponent stejný název.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="0b7bd-203">Chcete-li shromažďovat konkrétní podrobnosti o provádění mapování modelu elektronického výkaznictví a součástech formátu elektronického výkaznictví, nastavte následující možnosti na hodnotu **Ano**:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="0b7bd-204">**Shromáždit statistiky dotazů** – Pokud je tato možnost zapnuta, bude sledování výkonu bude shromažďovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="0b7bd-205">Počet volání databáze, která byla provedena zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="0b7bd-206">Počet duplicitních volání do databáze</span><span class="sxs-lookup"><span data-stu-id="0b7bd-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="0b7bd-207">Podrobnosti o příkazech SQL, které byly použity k vytvoření databázových volání</span><span class="sxs-lookup"><span data-stu-id="0b7bd-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="0b7bd-208">**Sledovat přístup ukládání do mezipaměti** - Je-li tato možnost zapnuta, bude sledování výkonu shromažďovat informace o využití mezipaměti mapování modelu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="0b7bd-209">**Přístup k datům sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu volání do databáze pro provedené zdroje dat typu seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="0b7bd-210">**Výčet seznamu sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu záznamů vyžadovaných od zdrojů dat typu seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b7bd-211">Parametry v dialogovém okně **Parametry uživatelů** jsou specifické pro uživatele a aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogové okno Parametry uživatele](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="0b7bd-213">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-213">Run the ER format</span></span>

1. <span data-ttu-id="0b7bd-214">Vyberte společnost **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="0b7bd-215">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="0b7bd-216">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="0b7bd-217">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="0b7bd-218">Povšimněte si, že vygenerovaný soubor uvádí informace o 265 transakcích pro šest dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="0b7bd-219">Kontrola sledování provádění</span><span class="sxs-lookup"><span data-stu-id="0b7bd-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="0b7bd-220">Export generovaného trasovacího programu z aplikace</span><span class="sxs-lookup"><span data-stu-id="0b7bd-220">Export the generated trace from the application</span></span>

<span data-ttu-id="0b7bd-221">Sledování výkonu je odděleno od zdrojového formátu elektronického výkaznictví a lze ho serializovat do externího souboru ZIP.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="0b7bd-222">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurovat protokoly ladění**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="0b7bd-223">Na stránce **Protokoly spuštění elektronického výkaznictví** v levém podokně v poli **Název konfigurace** vyberte **Formát sledování výkonu** pro vyhledání záznamů protokolů, které byly vygenerovány provedením konfigurace **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="0b7bd-224">Vyberte tlačítko **Přílohy** (ikona kancelářské sponky) v pravém horním rohu stránky, nebo stiskněte **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Tlačítko Přílohy na stránce Protokoly spuštění elektronického výkaznictví](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="0b7bd-226">Na stránce **Přílohy pro protokoly spuštění elektronického výkaznictví** v podokně akcí zvolte **Otevřít** pro získání sledování výkonu jako souboru ZIP, a lokálně ho uložte.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Přílohy pro protokoly spuštění elektronických sestav](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="0b7bd-228">Vygenerovaní sledování má odkaz na zdrojovou sestavu elektronického výkaznictví prostřednictvím jedinečného identifikátoru sestavy pouze ve formátu **GUID**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="0b7bd-229">Číslování verzí formátu není zvažováno.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="0b7bd-230">Všimněte si, že přidružení mezi sledováním výkonu, které bylo vygenerováno pro spuštěný formát elektronického výkaznictví, a mapováním modelu elektronického výkaznictví, je založeno na použitém kořenovém popisovači a na společném datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="0b7bd-231">Číslování verzí formátu a mapování modelu není zvažováno.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="0b7bd-232">Nastavení příznaku **Výchozí pro mapování modelu** pro mapování modelu se také nebere v úvahu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="0b7bd-233">Import generovaného sledování do RCS</span><span class="sxs-lookup"><span data-stu-id="0b7bd-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="0b7bd-234">V RCS v pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="0b7bd-235">Na stránce **Konfigurace** ve stromové struktuře konfigurací rozbalte položku **Model sledování výkonu** a vyberte položku **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="0b7bd-236">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="0b7bd-237">Na stránce **Návrhář formátu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="0b7bd-238">V dialogovém okně **Nastavení výsledků sledování výkonu** vyberte možnost **Importovat sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="0b7bd-239">Vyberte **Procházet** a vyberte soubor zip, který jste předtím exportovali.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="0b7bd-240">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-240">Select **OK**.</span></span>

    ![Dialogové okno nastavení výsledků sledování výkonu v RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="0b7bd-242">Použití sledování výkonu pro analýzu v RCS – provádění formátu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="0b7bd-243">V RCS na stránce **Návrhář formátu** vyberte možnost **Rozbalit/sbalit** a rozbalte obsah všech položek formátu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="0b7bd-244">Všimněte si, že pro některé položky aktuálního formátu jsou zobrazeny další informace:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="0b7bd-245">Skutečný čas strávený zadáváním dat ve vygenerovaném výstupu s použitím položky formátu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="0b7bd-246">Stejný čas vyjádřený jako procento z celkového času stráveného generováním celého výstupu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Stránka návrháře formátu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="0b7bd-248">Zavřete stránku **návrháře formátu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="0b7bd-249">Použití sledování výkonu pro analýzu v RCS – mapování modelu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="0b7bd-250">V RCS na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="0b7bd-251">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="0b7bd-252">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-252">Select **Designer**.</span></span>
4. <span data-ttu-id="0b7bd-253">Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="0b7bd-254">Vyberte sledování, které jste importovali dříve.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="0b7bd-255">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-255">Select **OK**.</span></span>

<span data-ttu-id="0b7bd-256">Povšimněte si, že nové informace budou k dispozici pro některé položky zdroje dat aktuálního mapování modelu:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="0b7bd-257">Skutečný čas strávený získáváním dat pomocí zdroje dat</span><span class="sxs-lookup"><span data-stu-id="0b7bd-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="0b7bd-258">Stejný čas vyjádřený jako procento z celkového času stráveného spouštěním celého mapování modelu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="0b7bd-259">Všimněte si, že elektronické výkaznictví vás informuje, že aktuální mapování modelu duplikuje databázové požadavky, zatímco je spuštěn zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="0b7bd-260">Tato duplicita nastane, protože seznam transakcí dodavatele se pro každý opakovaný záznam dodavatele volá dvakrát.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="0b7bd-261">Jedno volání se provádí pro zadání podrobností o každé transakci v datovém modelu na základě konfigurovaných vazeb.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="0b7bd-262">Druhé volání se provádí k zadání vypočítaného počtu transakcí pro dodavatele v datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Zpráva o duplicitních žádostech databáze na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="0b7bd-264">Hodnota **\[Q:530\]** označuje, že tabulka VendTrans byla volána 530krát, aby vracela záznam z této tabulky do datové zdroje VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="0b7bd-265">Hodnota **\[530\]** označuje, že zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum byl volán 530krát, aby vracel záznam z tohoto zdroje dat a zadal z něj podrobnosti do datového modelu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="0b7bd-266">Doporučujeme použít ukládání do mezipaměti pro datový zdroj VendTable/\<Relations/VendTrans.VendTable\_AccountNum ke snížení počtu volání, která jsou prováděna za účelem získání podrobností o 265 transakcích 265 a zlepšení výkonu mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="0b7bd-267">Je také užitečné omezit počet volání, která jsou provedena na zdroj dat LedgerTransTypeList.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="0b7bd-268">Tento zdroj dat slouží k přidružení každé hodnoty výčtu **LedgerTransType** k jeho popisku.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="0b7bd-269">Pomocí tohoto zdroje dat můžete vyhledat příslušný popisek a zadat ho do datového modelu pro každou transakci dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="0b7bd-270">Aktuální počet volání tohoto zdroje dat (9 027) je poměrně vysoký pro 265 transakcí.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Stránka návrháře mapování modelu v RCS, zobrazující 9 027 volání zdroje dat.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="0b7bd-272">Vylepšení mapování modelu na základě informací ze sledování provádění</span><span class="sxs-lookup"><span data-stu-id="0b7bd-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="0b7bd-273">Úprava logiky mapování modelu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="0b7bd-274">Chcete-li zabránit duplicitním voláním do databáze, postupujte podle následujících kroků pro použití ukládání do mezipaměti:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="0b7bd-275">V RCS na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte položku **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="0b7bd-276">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="0b7bd-277">Rozbalte položku **VendTable**, rozbalte seznam relací 1:N pro zdroj dat VendTable (položka **\<Vztahy**) a vyberte položku **VendTrans. VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="0b7bd-278">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-278">Select **Cache**.</span></span>

    ![Nastavení ukládání do mezipaměti za účelem předcházení duplicitním voláním](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="0b7bd-280">Chcete-li do rozsahu datového zdroje VendTable přenést zdroj dat LedgerTransTypeList, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="0b7bd-281">V podokně **Typy zdrojů dat** rozbalte položku **Funkce** a vyberte položku **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="0b7bd-282">V podokně **Datové zdroje** vyberte položku **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="0b7bd-283">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-283">Select **Add**.</span></span>
    4. <span data-ttu-id="0b7bd-284">Do pole **Název** zadejte řetězec **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="0b7bd-285">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="0b7bd-286">Do pole **Vzorec** zadejte **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="0b7bd-287">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-287">Select **Save**.</span></span>
    8. <span data-ttu-id="0b7bd-288">Zavřete stránku **Editor vzorců**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="0b7bd-289">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-289">Click **OK**.</span></span>

3. <span data-ttu-id="0b7bd-290">Chcete-li provést ukládání do mezipaměti pole **\$TransType**, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="0b7bd-291">Vyberte položku **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="0b7bd-292">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="0b7bd-293">Vyberte položku **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="0b7bd-294">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-294">Select **Cache**.</span></span>

    ![Nastavení ukládání do mezipaměti pro pole $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="0b7bd-296">Chcete-li změnit **\$TransTypeRecord** tak, aby začalo používat pole **\$TransType** uložené v mezipaměti, použijte následující postup:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="0b7bd-297">V podokně **Datové zdroje** rozbalte položku **VendTable**, rozbalte položku **\<Relations**, rozbalte položku **VendTrans.VendTable\_AccountNum** a vyberte položku **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="0b7bd-298">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="0b7bd-299">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="0b7bd-300">V poli **Vzorec** vyhledejte následující výraz:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="0b7bd-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="0b7bd-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="0b7bd-302">V poli **Vzorec** zadejte následující výraz:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="0b7bd-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="0b7bd-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="0b7bd-304">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-304">Select **Save**.</span></span>
    7. <span data-ttu-id="0b7bd-305">Zavřete stránku **Editor vzorců**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="0b7bd-306">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-306">Select **OK**.</span></span>

5. <span data-ttu-id="0b7bd-307">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-307">Select **Save**.</span></span>
6. <span data-ttu-id="0b7bd-308">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="0b7bd-309">Zavřete stránku **Mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="0b7bd-310">Dokončení upravené verze mapování modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="0b7bd-311">V RCS na stránce **Konfigurace** na záložce s náhledem **Verze** vyberte verzi **1.2** konfigurace **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="0b7bd-312">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-312">Select **Change status**.</span></span>
3. <span data-ttu-id="0b7bd-313">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="0b7bd-314">Import upravené konfigurace mapování modelu elektronického výkaznictví z RCS do aplikace</span><span class="sxs-lookup"><span data-stu-id="0b7bd-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="0b7bd-315">Opakujte kroky z části [Import konfigurace elektronického výkaznictví z RCS do Finance and Operations](#import-configuration) dříve v tomto tématu pro import verze 1.2 konfigurace **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="0b7bd-316">Spuštění upraveného řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="0b7bd-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="0b7bd-317">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-317">Run the ER format</span></span>

<span data-ttu-id="0b7bd-318">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="0b7bd-319">Práce se sledováním spuštění</span><span class="sxs-lookup"><span data-stu-id="0b7bd-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="0b7bd-320">Export generovaného trasovacího programu z aplikace</span><span class="sxs-lookup"><span data-stu-id="0b7bd-320">Export the generated trace from the application</span></span>

<span data-ttu-id="0b7bd-321">Zopakujte kroky v části [Exportování vygenerovaného sledování z aplikace](#export-trace) výše v tomto tématu pro místní uložení nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="0b7bd-322">Import generovaného sledování do RCS</span><span class="sxs-lookup"><span data-stu-id="0b7bd-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="0b7bd-323">Opakujte kroky v části [Import generovaného sledování do RCS](#import-trace) výše v tomto tématu pro import nového sledování výkonu do RCS.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="0b7bd-324">Použití sledování výkonu pro analýzu v RCS – mapování modelu</span><span class="sxs-lookup"><span data-stu-id="0b7bd-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="0b7bd-325">Opakujte kroky v části [Použití sledování výkonu pro analýzu v RCS – mapování modelu](#use-trace) výše v tomto tématu pro analýzu nejnovějšího sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="0b7bd-326">Všimněte si, že úpravy provedené v mapování modelu odstranily duplicitní dotazy do databáze.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="0b7bd-327">Počet volání databázových tabulek a zdrojů dat pro toto mapování modelu byl také snížen.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="0b7bd-328">Z toho vyplývá zvýšení výkonu celého řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Sledování informací pro datový zdroj VendTable na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="0b7bd-330">Hodnota **\[12\]** pro zdroj dat VendTable v informacích o sledování označuje, že tento zdroj dat byl volán 12krát.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="0b7bd-331">Hodnota **\[Q:6\]** označuje, že šest volání bylo přeloženo do volání databáze do tabulky VendTable.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="0b7bd-332">Hodnota **\[C:6\]** označuje, že záznamy načtené z databáze byly uloženy do mezipaměti a šest dalších volání bylo zpracováno pomocí mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="0b7bd-333">Všimněte si, že počet volání zdroje dat LedgerTransTypeList byl snížen z 9 027 na 240.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Sledování informací pro datový zdroj LedgerTransTypeList na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="0b7bd-335">Kontrola sledování spuštění v aplikaci</span><span class="sxs-lookup"><span data-stu-id="0b7bd-335">Review the execution trace in the application</span></span>

<span data-ttu-id="0b7bd-336">Kromě RCS mohou některé verze nabídnout možnosti pro rozhraní návrháře architektury elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="0b7bd-337">Tyto verze mají možnost **Povolit režim návrhu**, kterou lze zapnout.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="0b7bd-338">Tuto možnost naleznete na kartě **Obecné** na stránce **Parametry elektronického výkaznictví**, kterou lze otevřít v pracovním prostoru **elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Povolení možnosti režimu návrhu na stránce parametry elektronického vykazování](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="0b7bd-340">Pokud používáte některou z těchto verzí můžete analyzovat podrobnosti generovaných sledováních výkonu přímo v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="0b7bd-341">Nemusíte je exportovat z aplikace a importovat do RCS.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="0b7bd-342">Kontrola sledování provádění pomocí externích nástrojů</span><span class="sxs-lookup"><span data-stu-id="0b7bd-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="0b7bd-343">Konfigurace parametrů uživatele</span><span class="sxs-lookup"><span data-stu-id="0b7bd-343">Configure user parameters</span></span>

1. <span data-ttu-id="0b7bd-344">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="0b7bd-345">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0b7bd-346">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** v poli **Formát sledování provádění** vyberte **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="0b7bd-347">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-347">Run the ER format</span></span>

<span data-ttu-id="0b7bd-348">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="0b7bd-349">Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="0b7bd-350">Tento soubor obsahuje sledování výkonu ve formátu PerfView.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="0b7bd-351">Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Informace o sledování výkonu ve formátu PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="0b7bd-353">Použití externích nástrojů ke kontrole sledování provádění, které obsahuje databázové dotazy</span><span class="sxs-lookup"><span data-stu-id="0b7bd-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="0b7bd-354">Z důvodu vylepšení, které bylo provedeno v rámci architektury elektronického výkaznictví, nabízí sledování výkonu generované ve formátu PerfView nyní více podrobnostmi o provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="0b7bd-355">V aplikaci Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (červenec 2019) může toto sledování také zahrnovat podrobnosti o provedených dotazech SQL do aplikační databáze.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="0b7bd-356">Konfigurace parametrů uživatele</span><span class="sxs-lookup"><span data-stu-id="0b7bd-356">Configure user parameters</span></span>

1. <span data-ttu-id="0b7bd-357">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0b7bd-358">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0b7bd-359">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** nastavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="0b7bd-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="0b7bd-360">V poli **Formát sledování provádění** vyberte **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="0b7bd-361">Nastavte možnost **Shromáždit statistiky dotazů** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="0b7bd-362">Nastavte možnost **Dotaz na sledování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Sekce sledování spuštění, dialogové okno Parametry uživatelů](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="0b7bd-364">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-364">Run the ER format</span></span>

<span data-ttu-id="0b7bd-365">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="0b7bd-366">Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="0b7bd-367">Tento soubor obsahuje sledování výkonu ve formátu PerfView.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="0b7bd-368">Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="0b7bd-369">Sledování nyní zahrnuje podrobné informace o přístupu k databázi SQL během provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="0b7bd-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Informace o sledování pro spuštěný formát elektronického výkaznictví v PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="0b7bd-371">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0b7bd-371">Additional resources</span></span>

- [<span data-ttu-id="0b7bd-372">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="0b7bd-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0b7bd-373">Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE</span><span class="sxs-lookup"><span data-stu-id="0b7bd-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
