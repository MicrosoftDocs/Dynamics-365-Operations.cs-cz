---
title: Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem
description: Toto téma obsahuje informace o způsobu použití funkce sledování výkonu v elektronickém výkaznictví pro řešení potíží s výkonem.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 207783f5a44d5c6432539ac27a8c491bca811da4
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760024"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="89a33-103">Sledování provádění formátů elektronického výkaznictví za účelem řešení potíží s výkonem</span><span class="sxs-lookup"><span data-stu-id="89a33-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="89a33-104">V rámci procesu navrhování konfigurací elektronického výkaznictví pro generování elektronických dokumentů definujete metodu, která se používá k získání dat z aplikace a jejich zadávání do generovaného výstupu.</span><span class="sxs-lookup"><span data-stu-id="89a33-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="89a33-105">Funkce sledování výkonu elektronického výkaznictví pomáhá významně snižovat čas a náklady, které jsou spojeny se shromažďováním podrobností o provedení formátu elektronického výkaznictví a jejich použití k řešení potíží s výkonem.</span><span class="sxs-lookup"><span data-stu-id="89a33-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="89a33-106">Tento kurz poskytuje pokyny k interpretaci sledování výkonu pro provedené formáty elektronického výkaznictví a způsob použití informací z těchto sledování k vylepšení výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="89a33-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="89a33-107">Prerequisites</span></span>

<span data-ttu-id="89a33-108">Pro dokončení příkladů v tomto kurzu musíte mít následující přístup:</span><span class="sxs-lookup"><span data-stu-id="89a33-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="89a33-109">Přejděte k některé z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="89a33-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="89a33-110">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="89a33-111">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="89a33-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="89a33-112">System administrator</span></span>

- <span data-ttu-id="89a33-113">Přístup k instanci služeb Regulatory Configuration Services (RCS), který byl zřízen pro stejného klienta jako aplikace, pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="89a33-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="89a33-114">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="89a33-115">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="89a33-116">Správce systému</span><span class="sxs-lookup"><span data-stu-id="89a33-116">System administrator</span></span>

<span data-ttu-id="89a33-117">Je také nutné stáhnout a lokálně uložit následující soubory.</span><span class="sxs-lookup"><span data-stu-id="89a33-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="89a33-118">Soubor</span><span class="sxs-lookup"><span data-stu-id="89a33-118">File</span></span>                                  | <span data-ttu-id="89a33-119">Obsah</span><span class="sxs-lookup"><span data-stu-id="89a33-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="89a33-120">Model sledování výkonu - verze 1</span><span class="sxs-lookup"><span data-stu-id="89a33-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="89a33-121">Vzorová konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="89a33-122">Metadata sledování výkonu - verze 1</span><span class="sxs-lookup"><span data-stu-id="89a33-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="89a33-123">Vzorová konfigurace metadat elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="89a33-124">Mapování sledování výkonu - verze 1.1</span><span class="sxs-lookup"><span data-stu-id="89a33-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="89a33-125">Vzorová konfigurace mapování elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="89a33-126">Formát sledování výkonu - verze 1.1</span><span class="sxs-lookup"><span data-stu-id="89a33-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="89a33-127">Vzorová konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="89a33-128">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="89a33-128">Configure ER parameters</span></span>

<span data-ttu-id="89a33-129">Každé sledování výkonu elektronického výkaznictví, které je generováno v aplikaci, je uloženo jako příloha záznamu protokolu provádění.</span><span class="sxs-lookup"><span data-stu-id="89a33-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="89a33-130">Pro správu těchto příloh se používá architektura správy dokumentů (DM).</span><span class="sxs-lookup"><span data-stu-id="89a33-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="89a33-131">Parametry elektronického výkaznictví je nutné nakonfigurovat s předstihem, aby bylo možné určit typ dokumentu ve správě dokumentů, který se má použít pro připojení sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="89a33-132">V pracovním prostoru **Elektronické sestavy** vyberte **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="89a33-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="89a33-133">Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.</span><span class="sxs-lookup"><span data-stu-id="89a33-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Stránka parametrů elektronického výkaznictví](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="89a33-135">Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):</span><span class="sxs-lookup"><span data-stu-id="89a33-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="89a33-136">**Třída:** Připojit soubor</span><span class="sxs-lookup"><span data-stu-id="89a33-136">**Class:** Attach file</span></span>
- <span data-ttu-id="89a33-137">**Skupina:** Soubor</span><span class="sxs-lookup"><span data-stu-id="89a33-137">**Group:** File</span></span>

![Stránka typu dokumentu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="89a33-139">Vybraný typ dokumentu musí být k dispozici ve všech společnostech aktuální instance, protože přílohy správy dokumentů jsou specifické pro konkrétní společnost.</span><span class="sxs-lookup"><span data-stu-id="89a33-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="89a33-140">Konfigurace parametrů RCS</span><span class="sxs-lookup"><span data-stu-id="89a33-140">Configure RCS parameters</span></span>

<span data-ttu-id="89a33-141">Sledování výkonu elektronického výkaznictví, která jsou generována, budou importována do RCS pro analýzu pomocí návrháře formátu elektronického výkaznictví a návrháře mapování elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="89a33-142">Vzhledem k tomu, že sledování výkonu elektronického výkaznictví jsou uložena jako přílohy záznamu protokolu spouštění, který souvisí s formátem elektronického výkaznictví, je nutné předem nakonfigurovat parametry RCS, aby bylo možné určit typ dokumentu správy dokumentů, který se má použít pro připojení sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="89a33-143">V instanci RCS zřízené pro vaši společnost vyberte v pracovním prostoru **Elektronické výkaznictví** možnost **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="89a33-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="89a33-144">Poté na stránce **Parametry elektronického výkaznictví** na kartě **Přílohy** v poli **Jiné** vyberte dokument správy dokumentů pro použití sledování výkonů.</span><span class="sxs-lookup"><span data-stu-id="89a33-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Stránka parametrů elektronického výkaznictví v RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="89a33-146">Aby byl k dispozici ve vyhledávacím poli **Jiné**, musí být typ dokumentu typu správy dokumentů nakonfigurován následujícím způsobem na stránce **Typy dokumentů** (**Správa organizace \> Správa dokumentů \> Typy dokumentů**):</span><span class="sxs-lookup"><span data-stu-id="89a33-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="89a33-147">**Třída:** Připojit soubor</span><span class="sxs-lookup"><span data-stu-id="89a33-147">**Class:** Attach file</span></span>
- <span data-ttu-id="89a33-148">**Skupina:** Soubor</span><span class="sxs-lookup"><span data-stu-id="89a33-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="89a33-149">Návrh řešení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-149">Design an ER solution</span></span>

<span data-ttu-id="89a33-150">Předpokládejme, že jste začali navrhovat nové řešení elektronického výkaznictví pro generování nové sestavy, která představuje transakce dodavatele.</span><span class="sxs-lookup"><span data-stu-id="89a33-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="89a33-151">Momentálně můžete najít transakce pro zvoleného dodavatele na stránce **Transakce dodavatele** (přejděte na **Závazky \> Dodavatelé \> Všichni dodavatelé**, zvolte dodavatele a potom v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Transakce**).</span><span class="sxs-lookup"><span data-stu-id="89a33-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="89a33-152">Chcete však mít všechny transakce dodavatele současně v jednom elektronickém dokumentu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="89a33-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="89a33-153">Toto řešení bude obsahovat několik konfigurací elektronického výkaznictví, které obsahují požadovaný datový model, metadata, mapování modelu a součásti formátu.</span><span class="sxs-lookup"><span data-stu-id="89a33-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="89a33-154">Přihlaste se k instanci RCS, která byla pro vaši společnost zřízena.</span><span class="sxs-lookup"><span data-stu-id="89a33-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="89a33-155">V tomto kurzu vytvoříte a upravíte konfigurace pro vzorovou společnost **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="89a33-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="89a33-156">Proto se ujistěte, že tento poskytovatel konfigurace byl přidán do RCS a vybrán jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="89a33-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="89a33-157">Pokyny naleznete v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="89a33-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="89a33-158">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="89a33-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="89a33-159">Na stránce **Konfigurace** importujte konfigurace elektronického výkaznictví, které jste stáhli jako nezbytný požadavek do RCS, v následujícím pořadí: datový model, metadata, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="89a33-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="89a33-160">Pro každou konfiguraci postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="89a33-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="89a33-161">V podokně akcí vyberte **Exchange \> Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="89a33-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="89a33-162">Zvolte **Procházet** a vyberte příslušný soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="89a33-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="89a33-163">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="89a33-163">Select **OK**.</span></span>

    ![Stránka konfigurace v RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="89a33-165">Spuštění řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="89a33-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="89a33-166">Předpokládejme, že jste dokončili návrh první verze řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="89a33-167">Nyní ji chcete vyzkoušet ve své instanci a analyzovat výkon provedení.</span><span class="sxs-lookup"><span data-stu-id="89a33-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="89a33-168">Import konfigurace elektronického výkaznictví z RCS do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="89a33-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="89a33-169">Přihlaste se k instanci aplikace.</span><span class="sxs-lookup"><span data-stu-id="89a33-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="89a33-170">V tomto kurzu naimportujete konfigurace z vaší instance RCS (kde navrhujete komponenty elektronického výkaznictví) do své instance (kde je otestujete a nakonec je použijete).</span><span class="sxs-lookup"><span data-stu-id="89a33-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="89a33-171">Proto je nutné zajistit, aby byly připraveny všechny požadované artefakty.</span><span class="sxs-lookup"><span data-stu-id="89a33-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="89a33-172">Další pokyny získáte v postupu [Import konfigurací elektronického výkaznictví ze služby RCS (Regulatory Configuration Services)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="89a33-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="89a33-173">Pomocí následujícího postupu importujte konfigurace z RCS do aplikace:</span><span class="sxs-lookup"><span data-stu-id="89a33-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="89a33-174">V pracovním prostoru **Elektronické výkaznictví** na dlaždici pro poskytovatele konfigurace **Litware, Inc** . vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="89a33-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="89a33-175">Na stránce **Úložiště konfigurací** vyberte úložiště typu **RCS** a poté zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="89a33-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="89a33-176">Na záložce s náhledem **Konfigurace** vyberte konfiguraci **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="89a33-177">Na záložce s náhledem **Verze** zvolte verzi **1.1** zvolené konfigurace a poté zvolte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="89a33-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Stránka úložiště konfigurace](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="89a33-179">Odpovídající verze konfigurací datových modelů a mapování modelů jsou automaticky importovány jako předpoklady pro importovanou konfiguraci formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="89a33-180">Zapnutí sledování výkonu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="89a33-181">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="89a33-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="89a33-182">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="89a33-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="89a33-183">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="89a33-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="89a33-184">V poli **Formát sledování provádění** zvolte **Ladit formát sledování** pro spuštění shromažďování podrobností o provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="89a33-185">Je-li vybrána tato hodnota, sledování výkonu bude shromažďovat informace o době strávené na následujících akcích:</span><span class="sxs-lookup"><span data-stu-id="89a33-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="89a33-186">Spuštění každého zdroje dat v mapování modelu, které je voláno za účelem získání dat</span><span class="sxs-lookup"><span data-stu-id="89a33-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="89a33-187">Zpracování jednotlivých položek formátu za účelem zadání dat ve výstupu, který je generován</span><span class="sxs-lookup"><span data-stu-id="89a33-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="89a33-188">Pole **Formát sledování provádění** použijte k upřesnění formátu generovaného sledování výkonu, ve kterém jsou uloženy podrobnosti o provádění pro formát elektronického výkaznictví a prvky mapování.</span><span class="sxs-lookup"><span data-stu-id="89a33-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="89a33-189">Volbou možnosti **adit formát sledování** budete moci analyzovat obsah sledování v návrháři operací elektronického výkaznictví a zobrazit formát elektronického výkaznictví nebo prvky mapování, které jsou uvedeny ve sledování.</span><span class="sxs-lookup"><span data-stu-id="89a33-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="89a33-190">Chcete-li shromažďovat konkrétní podrobnosti o provádění mapování modelu elektronického výkaznictví a součástech formátu elektronického výkaznictví, nastavte následující možnosti na hodnotu **Ano**:</span><span class="sxs-lookup"><span data-stu-id="89a33-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="89a33-191">**Shromáždit statistiky dotazů** – Pokud je tato možnost zapnuta, bude sledování výkonu bude shromažďovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="89a33-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="89a33-192">Počet volání databáze, která byla provedena zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="89a33-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="89a33-193">Počet duplicitních volání do databáze</span><span class="sxs-lookup"><span data-stu-id="89a33-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="89a33-194">Podrobnosti o příkazech SQL, které byly použity k vytvoření databázových volání</span><span class="sxs-lookup"><span data-stu-id="89a33-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="89a33-195">**Sledovat přístup ukládání do mezipaměti** - Je-li tato možnost zapnuta, bude sledování výkonu shromažďovat informace o využití mezipaměti mapování modelu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="89a33-196">**Přístup k datům sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu volání do databáze pro provedené zdroje dat typu seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="89a33-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="89a33-197">**Výčet seznamu sledování** – Pokud je tato možnost zapnuta, sledování výkonu bude shromažďovat informace o počtu záznamů vyžadovaných od zdrojů dat typu seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="89a33-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="89a33-198">Parametry v dialogovém okně **Parametry uživatelů** jsou specifické pro uživatele a aktuální společnost.</span><span class="sxs-lookup"><span data-stu-id="89a33-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogové okno Parametry uživatele](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="89a33-200">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-200">Run the ER format</span></span>

1. <span data-ttu-id="89a33-201">Vyberte společnost **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="89a33-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="89a33-202">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="89a33-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="89a33-203">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="89a33-204">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="89a33-205">Povšimněte si, že vygenerovaný soubor uvádí informace o 265 transakcích pro šest dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="89a33-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="89a33-206">Kontrola sledování provádění</span><span class="sxs-lookup"><span data-stu-id="89a33-206">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="89a33-207">Export generovaného trasovacího programu z aplikace</span><span class="sxs-lookup"><span data-stu-id="89a33-207">Export the generated trace from the application</span></span>

<span data-ttu-id="89a33-208">Sledování výkonu je odděleno od zdrojového formátu elektronického výkaznictví a lze ho serializovat do externího souboru ZIP.</span><span class="sxs-lookup"><span data-stu-id="89a33-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="89a33-209">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurovat protokoly ladění**.</span><span class="sxs-lookup"><span data-stu-id="89a33-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="89a33-210">Na stránce **Protokoly spuštění elektronického výkaznictví** v levém podokně v poli **Název konfigurace** vyberte **Formát sledování výkonu** pro vyhledání záznamů protokolů, které byly vygenerovány provedením konfigurace **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="89a33-211">Vyberte tlačítko **Přílohy** (ikona kancelářské sponky) v pravém horním rohu stránky, nebo stiskněte **Ctrl+Shift+A**.</span><span class="sxs-lookup"><span data-stu-id="89a33-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Tlačítko Přílohy na stránce Protokoly spuštění elektronického výkaznictví](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="89a33-213">Na stránce **Přílohy pro protokoly spuštění elektronického výkaznictví** v podokně akcí zvolte **Otevřít** pro získání sledování výkonu jako souboru ZIP, a lokálně ho uložte.</span><span class="sxs-lookup"><span data-stu-id="89a33-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Přílohy pro protokoly spuštění elektronických sestav](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="89a33-215">Vygenerovaní sledování má odkaz na zdrojovou sestavu elektronického výkaznictví prostřednictvím jedinečného identifikátoru sestavy pouze ve formátu **GUID**.</span><span class="sxs-lookup"><span data-stu-id="89a33-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="89a33-216">Číslování verzí formátu není zvažováno.</span><span class="sxs-lookup"><span data-stu-id="89a33-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="89a33-217">Všimněte si, že přidružení mezi sledováním výkonu, které bylo vygenerováno pro spuštěný formát elektronického výkaznictví, a mapováním modelu elektronického výkaznictví, je založeno na použitém kořenovém popisovači a na společném datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="89a33-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="89a33-218">Číslování verzí formátu a mapování modelu není zvažováno.</span><span class="sxs-lookup"><span data-stu-id="89a33-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="89a33-219">Nastavení příznaku **Výchozí pro mapování modelu** pro mapování modelu se také nebere v úvahu.</span><span class="sxs-lookup"><span data-stu-id="89a33-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="89a33-220">Import generovaného sledování do RCS</span><span class="sxs-lookup"><span data-stu-id="89a33-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="89a33-221">V RCS v pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="89a33-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="89a33-222">Na stránce **Konfigurace** ve stromové struktuře konfigurací rozbalte položku **Model sledování výkonu** a vyberte položku **Formát sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="89a33-223">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="89a33-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="89a33-224">Na stránce **Návrhář formátu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="89a33-225">V dialogovém okně **Nastavení výsledků sledování výkonu** vyberte možnost **Importovat sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="89a33-226">Vyberte **Procházet** a vyberte soubor zip, který jste předtím exportovali.</span><span class="sxs-lookup"><span data-stu-id="89a33-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="89a33-227">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="89a33-227">Select **OK**.</span></span>

    ![Dialogové okno nastavení výsledků sledování výkonu v RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="89a33-229">Použití sledování výkonu pro analýzu v RCS – provádění formátu</span><span class="sxs-lookup"><span data-stu-id="89a33-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="89a33-230">V RCS na stránce **Návrhář formátu** vyberte možnost **Rozbalit/sbalit** a rozbalte obsah všech položek formátu.</span><span class="sxs-lookup"><span data-stu-id="89a33-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="89a33-231">Všimněte si, že pro některé položky aktuálního formátu jsou zobrazeny další informace:</span><span class="sxs-lookup"><span data-stu-id="89a33-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="89a33-232">Skutečný čas strávený zadáváním dat ve vygenerovaném výstupu s použitím položky formátu</span><span class="sxs-lookup"><span data-stu-id="89a33-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="89a33-233">Stejný čas vyjádřený jako procento z celkového času stráveného generováním celého výstupu</span><span class="sxs-lookup"><span data-stu-id="89a33-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Stránka návrháře formátu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="89a33-235">Zavřete stránku **návrháře formátu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-235">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="89a33-236">Použití sledování výkonu pro analýzu v RCS – mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89a33-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="89a33-237">V RCS na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="89a33-238">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="89a33-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="89a33-239">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="89a33-239">Select **Designer**.</span></span>
4. <span data-ttu-id="89a33-240">Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="89a33-241">Vyberte sledování, které jste importovali dříve.</span><span class="sxs-lookup"><span data-stu-id="89a33-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="89a33-242">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="89a33-242">Select **OK**.</span></span>

<span data-ttu-id="89a33-243">Povšimněte si, že nové informace budou k dispozici pro některé položky zdroje dat aktuálního mapování modelu:</span><span class="sxs-lookup"><span data-stu-id="89a33-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="89a33-244">Skutečný čas strávený získáváním dat pomocí zdroje dat</span><span class="sxs-lookup"><span data-stu-id="89a33-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="89a33-245">Stejný čas vyjádřený jako procento z celkového času stráveného spouštěním celého mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89a33-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="89a33-246">Všimněte si, že elektronické výkaznictví vás informuje, že aktuální mapování modelu duplikuje databázové požadavky, zatímco je spuštěn zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="89a33-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="89a33-247">Tato duplicita nastane, protože seznam transakcí dodavatele se pro každý opakovaný záznam dodavatele volá dvakrát.</span><span class="sxs-lookup"><span data-stu-id="89a33-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="89a33-248">Jedno volání se provádí pro zadání podrobností o každé transakci v datovém modelu na základě konfigurovaných vazeb.</span><span class="sxs-lookup"><span data-stu-id="89a33-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="89a33-249">Druhé volání se provádí k zadání vypočítaného počtu transakcí pro dodavatele v datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="89a33-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Zpráva o duplicitních žádostech databáze na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="89a33-251">Hodnota **\[Q:530\]** označuje, že tabulka VendTrans byla volána 530krát, aby vracela záznam z této tabulky do datové zdroje VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="89a33-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="89a33-252">Hodnota **\[530\]** označuje, že zdroj dat VendTable/\<Relations/VendTrans.VendTable\_AccountNum byl volán 530krát, aby vracel záznam z tohoto zdroje dat a zadal z něj podrobnosti do datového modelu.</span><span class="sxs-lookup"><span data-stu-id="89a33-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="89a33-253">Doporučujeme použít ukládání do mezipaměti pro datový zdroj VendTable/\<Relations/VendTrans.VendTable\_AccountNum ke snížení počtu volání, která jsou prováděna za účelem získání podrobností o 265 transakcích 265 a zlepšení výkonu mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="89a33-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="89a33-254">Je také užitečné omezit počet volání, která jsou provedena na zdroj dat LedgerTransTypeList.</span><span class="sxs-lookup"><span data-stu-id="89a33-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="89a33-255">Tento zdroj dat slouží k přidružení každé hodnoty výčtu **LedgerTransType** k jeho popisku.</span><span class="sxs-lookup"><span data-stu-id="89a33-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="89a33-256">Pomocí tohoto zdroje dat můžete vyhledat příslušný popisek a zadat ho do datového modelu pro každou transakci dodavatele.</span><span class="sxs-lookup"><span data-stu-id="89a33-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="89a33-257">Aktuální počet volání tohoto zdroje dat (9 027) je poměrně vysoký pro 265 transakcí.</span><span class="sxs-lookup"><span data-stu-id="89a33-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Stránka návrháře mapování modelu v RCS, zobrazující 9 027 volání zdroje dat.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="89a33-259">Vylepšení mapování modelu na základě informací ze sledování provádění</span><span class="sxs-lookup"><span data-stu-id="89a33-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="89a33-260">Úprava logiky mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89a33-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="89a33-261">Chcete-li zabránit duplicitním voláním do databáze, postupujte podle následujících kroků pro použití ukládání do mezipaměti:</span><span class="sxs-lookup"><span data-stu-id="89a33-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="89a33-262">V RCS na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte položku **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="89a33-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="89a33-263">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="89a33-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="89a33-264">Rozbalte položku **VendTable**, rozbalte seznam relací 1:N pro zdroj dat VendTable (položka **\<Vztahy**) a vyberte položku **VendTrans. VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="89a33-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="89a33-265">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="89a33-265">Select **Cache**.</span></span>

    ![Nastavení ukládání do mezipaměti za účelem předcházení duplicitním voláním](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="89a33-267">Chcete-li do rozsahu datového zdroje VendTable přenést zdroj dat LedgerTransTypeList, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="89a33-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="89a33-268">V podokně **Typy zdrojů dat** rozbalte položku **Funkce** a vyberte položku **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="89a33-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="89a33-269">V podokně **Datové zdroje** vyberte položku **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="89a33-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="89a33-270">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="89a33-270">Select **Add**.</span></span>
    4. <span data-ttu-id="89a33-271">Do pole **Název** zadejte řetězec **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="89a33-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="89a33-272">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="89a33-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="89a33-273">Do pole **Vzorec** zadejte **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="89a33-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="89a33-274">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-274">Select **Save**.</span></span>
    8. <span data-ttu-id="89a33-275">Zavřete stránku **Editor vzorců**.</span><span class="sxs-lookup"><span data-stu-id="89a33-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="89a33-276">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="89a33-276">Click **OK**.</span></span>

3. <span data-ttu-id="89a33-277">Chcete-li provést ukládání do mezipaměti pole **\$TransType**, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="89a33-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="89a33-278">Vyberte položku **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="89a33-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="89a33-279">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="89a33-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="89a33-280">Vyberte položku **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="89a33-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="89a33-281">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="89a33-281">Select **Cache**.</span></span>

    ![Nastavení ukládání do mezipaměti pro pole $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="89a33-283">Chcete-li změnit **\$TransTypeRecord** tak, aby začalo používat pole **\$TransType** uložené v mezipaměti, použijte následující postup:</span><span class="sxs-lookup"><span data-stu-id="89a33-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="89a33-284">V podokně **Datové zdroje** rozbalte položku **VendTable**, rozbalte položku **\<Relations**, rozbalte položku **VendTrans.VendTable\_AccountNum** a vyberte položku **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="89a33-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="89a33-285">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="89a33-286">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="89a33-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="89a33-287">V poli **Vzorec** vyhledejte následující výraz:</span><span class="sxs-lookup"><span data-stu-id="89a33-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="89a33-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="89a33-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="89a33-289">V poli **Vzorec** zadejte následující výraz:</span><span class="sxs-lookup"><span data-stu-id="89a33-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="89a33-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="89a33-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="89a33-291">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-291">Select **Save**.</span></span>
    7. <span data-ttu-id="89a33-292">Zavřete stránku **Editor vzorců**.</span><span class="sxs-lookup"><span data-stu-id="89a33-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="89a33-293">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="89a33-293">Select **OK**.</span></span>

5. <span data-ttu-id="89a33-294">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-294">Select **Save**.</span></span>
6. <span data-ttu-id="89a33-295">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="89a33-296">Zavřete stránku **Mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="89a33-297">Dokončení upravené verze mapování modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="89a33-298">V RCS na stránce **Konfigurace** na záložce s náhledem **Verze** vyberte verzi **1.2** konfigurace **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="89a33-299">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="89a33-299">Select **Change status**.</span></span>
3. <span data-ttu-id="89a33-300">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="89a33-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="89a33-301">Import upravené konfigurace mapování modelu elektronického výkaznictví z RCS do aplikace</span><span class="sxs-lookup"><span data-stu-id="89a33-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="89a33-302">Opakujte kroky z části [Import konfigurace elektronického výkaznictví z RCS do Finance and Operations](#import-configuration) dříve v tomto tématu pro import verze 1.2 konfigurace **Mapování sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="89a33-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="89a33-303">Spuštění upraveného řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="89a33-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="89a33-304">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-304">Run the ER format</span></span>

<span data-ttu-id="89a33-305">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="89a33-306">Práce se sledováním spuštění</span><span class="sxs-lookup"><span data-stu-id="89a33-306">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="89a33-307">Export generovaného trasovacího programu z aplikace</span><span class="sxs-lookup"><span data-stu-id="89a33-307">Export the generated trace from the application</span></span>

<span data-ttu-id="89a33-308">Zopakujte kroky v části [Exportování vygenerovaného sledování z aplikace](#export-trace) výše v tomto tématu pro místní uložení nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="89a33-309">Import generovaného sledování do RCS</span><span class="sxs-lookup"><span data-stu-id="89a33-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="89a33-310">Opakujte kroky v části [Import generovaného sledování do RCS](#import-trace) výše v tomto tématu pro import nového sledování výkonu do RCS.</span><span class="sxs-lookup"><span data-stu-id="89a33-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="89a33-311">Použití sledování výkonu pro analýzu v RCS – mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89a33-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="89a33-312">Opakujte kroky v části [Použití sledování výkonu pro analýzu v RCS – mapování modelu](#use-trace) výše v tomto tématu pro analýzu nejnovějšího sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="89a33-313">Všimněte si, že úpravy provedené v mapování modelu odstranily duplicitní dotazy do databáze.</span><span class="sxs-lookup"><span data-stu-id="89a33-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="89a33-314">Počet volání databázových tabulek a zdrojů dat pro toto mapování modelu byl také snížen.</span><span class="sxs-lookup"><span data-stu-id="89a33-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="89a33-315">Z toho vyplývá zvýšení výkonu celého řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Sledování informací pro datový zdroj VendTable na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="89a33-317">Hodnota **\[12\]** pro zdroj dat VendTable v informacích o sledování označuje, že tento zdroj dat byl volán 12krát.</span><span class="sxs-lookup"><span data-stu-id="89a33-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="89a33-318">Hodnota **\[Q:6\]** označuje, že šest volání bylo přeloženo do volání databáze do tabulky VendTable.</span><span class="sxs-lookup"><span data-stu-id="89a33-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="89a33-319">Hodnota **\[C:6\]** označuje, že záznamy načtené z databáze byly uloženy do mezipaměti a šest dalších volání bylo zpracováno pomocí mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="89a33-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="89a33-320">Všimněte si, že počet volání zdroje dat LedgerTransTypeList byl snížen z 9 027 na 240.</span><span class="sxs-lookup"><span data-stu-id="89a33-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Sledování informací pro datový zdroj LedgerTransTypeList na stránce návrháře mapování modelu v RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="89a33-322">Kontrola sledování spuštění v aplikaci</span><span class="sxs-lookup"><span data-stu-id="89a33-322">Review the execution trace in the application</span></span>

<span data-ttu-id="89a33-323">Kromě RCS mohou některé verze nabídnout možnosti pro rozhraní návrháře architektury elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="89a33-324">Tyto verze mají možnost **Povolit režim návrhu**, kterou lze zapnout.</span><span class="sxs-lookup"><span data-stu-id="89a33-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="89a33-325">Tuto možnost naleznete na kartě **Obecné** na stránce **Parametry elektronického výkaznictví**, kterou lze otevřít v pracovním prostoru **elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="89a33-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Povolení možnosti režimu návrhu na stránce parametry elektronického vykazování](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="89a33-327">Pokud používáte některou z těchto verzí můžete analyzovat podrobnosti generovaných sledováních výkonu přímo v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="89a33-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="89a33-328">Nemusíte je exportovat z aplikace a importovat do RCS.</span><span class="sxs-lookup"><span data-stu-id="89a33-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="89a33-329">Kontrola sledování provádění pomocí externích nástrojů</span><span class="sxs-lookup"><span data-stu-id="89a33-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="89a33-330">Konfigurace parametrů uživatele</span><span class="sxs-lookup"><span data-stu-id="89a33-330">Configure user parameters</span></span>

1. <span data-ttu-id="89a33-331">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="89a33-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="89a33-332">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="89a33-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="89a33-333">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** v poli **Formát sledování provádění** vyberte **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="89a33-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="89a33-334">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-334">Run the ER format</span></span>

<span data-ttu-id="89a33-335">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="89a33-336">Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení.</span><span class="sxs-lookup"><span data-stu-id="89a33-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="89a33-337">Tento soubor obsahuje sledování výkonu ve formátu PerfView.</span><span class="sxs-lookup"><span data-stu-id="89a33-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="89a33-338">Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Informace o sledování výkonu ve formátu PerfView](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="89a33-340">Použití externích nástrojů ke kontrole sledování provádění, které obsahuje databázové dotazy</span><span class="sxs-lookup"><span data-stu-id="89a33-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="89a33-341">Z důvodu vylepšení, které bylo provedeno v rámci architektury elektronického výkaznictví, nabízí sledování výkonu generované ve formátu PerfView nyní více podrobnostmi o provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="89a33-342">V aplikaci Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (červenec 2019) může toto sledování také zahrnovat podrobnosti o provedených dotazech SQL do aplikační databáze.</span><span class="sxs-lookup"><span data-stu-id="89a33-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="89a33-343">Konfigurace parametrů uživatele</span><span class="sxs-lookup"><span data-stu-id="89a33-343">Configure user parameters</span></span>

1. <span data-ttu-id="89a33-344">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="89a33-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="89a33-345">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="89a33-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="89a33-346">V dialogovém okně **Parametry uživatelů** v části **Sledování provádění** nastavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="89a33-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="89a33-347">V poli **Formát sledování provádění** vyberte **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="89a33-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="89a33-348">Nastavte možnost **Shromáždit statistiky dotazů** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="89a33-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="89a33-349">Nastavte možnost **Dotaz na sledování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="89a33-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Sekce sledování spuštění, dialogové okno Parametry uživatelů](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="89a33-351">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-351">Run the ER format</span></span>

<span data-ttu-id="89a33-352">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="89a33-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="89a33-353">Povšimněte si, že webový prohlížeč nabízí soubor zip ke stažení.</span><span class="sxs-lookup"><span data-stu-id="89a33-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="89a33-354">Tento soubor obsahuje sledování výkonu ve formátu PerfView.</span><span class="sxs-lookup"><span data-stu-id="89a33-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="89a33-355">Poté můžete pomocí nástroje analýzy výkonu PerfView analyzovat podrobnosti provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="89a33-356">Sledování nyní zahrnuje podrobné informace o přístupu k databázi SQL během provádění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89a33-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Informace o sledování pro spuštěný formát elektronického výkaznictví v PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="89a33-358">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="89a33-358">Additional resources</span></span>

- [<span data-ttu-id="89a33-359">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89a33-359">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="89a33-360">Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE</span><span class="sxs-lookup"><span data-stu-id="89a33-360">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)
