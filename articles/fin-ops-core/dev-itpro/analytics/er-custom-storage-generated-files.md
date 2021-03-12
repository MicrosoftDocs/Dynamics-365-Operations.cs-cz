---
title: Určení vlastních umístění úložišť pro vygenerované dokumenty
description: Toto téma vysvětluje, jak rozšířit seznam umístění úložišť pro dokumenty generované formáty elektronického výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680751"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="69660-103">Určení vlastních umístění úložišť pro vygenerované dokumenty</span><span class="sxs-lookup"><span data-stu-id="69660-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69660-104">Aplikační programovací rozhraní (API) rozhraní elektronického výkaznictví umožňuje rozšířit seznam umístění úložišť pro dokumenty, které generují ER formáty.</span><span class="sxs-lookup"><span data-stu-id="69660-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="69660-105">Toto téma vysvětluje, jak přidat vlastní umístění úložiště pro generované dokumenty delegováním úkolu vytváření cílů ER na výchozí cílový objekt pro vytváření a následnou implementací vlastní třídy, která má vlastní logiku cíle.</span><span class="sxs-lookup"><span data-stu-id="69660-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69660-106">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="69660-106">Prerequisites</span></span>

<span data-ttu-id="69660-107">Nasaďte topologii, která podporuje průběžné sestavování.</span><span class="sxs-lookup"><span data-stu-id="69660-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="69660-108">Další informace naleznete v tématu [Nasazení topologií, které podporují automatizaci průběžného sestavení a testů](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="69660-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="69660-109">Také musí mít přístup k této topologii pro jednu z následujících rolí.</span><span class="sxs-lookup"><span data-stu-id="69660-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="69660-110">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="69660-110">Electronic reporting developer</span></span>
- <span data-ttu-id="69660-111">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="69660-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="69660-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="69660-112">System administrator</span></span>

<span data-ttu-id="69660-113">Také musí mít přístup k vývojovému prostředí pro tuto topologii.</span><span class="sxs-lookup"><span data-stu-id="69660-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="69660-114">Všechny úkoly v tomto tématu lze dokončit ve společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="69660-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="69660-115">Import formátu ER dopředného posunutí dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="69660-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="69660-116">Chcete-li vygenerovat dokumenty, u kterých plánujete přidat vlastní umístění úložiště, [importujte](er-download-configurations-global-repo.md) konfiguraci formátu ER **Dopředné posunutí dlouhodobého majetku** do aktuální topologie.</span><span class="sxs-lookup"><span data-stu-id="69660-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Stránka úložiště konfigurace](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="69660-118">Spuštění sestavy dopředného posunutí dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="69660-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="69660-119">Přejděte do nabídky **Dlouhodobý majetek** \> **Dotazy a sestavy** \> **Sestavy transakcí** \> **Dopředné posunutí dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="69660-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="69660-120">V poli **Od data** zadejte **1/1/2017** (1. leden 2017).</span><span class="sxs-lookup"><span data-stu-id="69660-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="69660-121">V poli **Do data** zadejte **1/31/2017** (31. leden 2017).</span><span class="sxs-lookup"><span data-stu-id="69660-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="69660-122">V poli **Měna** vyberte hodnotu **Zúčtovací měna**.</span><span class="sxs-lookup"><span data-stu-id="69660-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="69660-123">V poli **Mapování formátu** vyberte **Dopředné posunutí dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="69660-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="69660-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="69660-124">Select **OK**.</span></span>

![Dialogové okno modulu runtime pro sestavu dopředného posunutí dlouhodobého majetku](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="69660-126">v aplikaci Microsoft Excel zkontrolujte odchozí dokument, který je generován a je k dispozici ke stažení.</span><span class="sxs-lookup"><span data-stu-id="69660-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="69660-127">Toto chování je [výchozí](electronic-reporting-destinations.md#default-behavior) pro formát ER, který nemá konfigurovány žádné [cíle](electronic-reporting-destinations.md) a běží v interaktivním režimu.</span><span class="sxs-lookup"><span data-stu-id="69660-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="69660-128">Kontrola zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="69660-128">Review the source code</span></span>

<span data-ttu-id="69660-129">Zkontrolujte kód metody `generateReportByGER()` třídy `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="69660-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="69660-130">Všimněte si, že k volání architektury ER a generování sestavy **Dopředné posunutí dlouhodobého majetku** se používá metoda `Run()`.</span><span class="sxs-lookup"><span data-stu-id="69660-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
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

## <a name="modify-the-source-code"></a><span data-ttu-id="69660-131">Úprava zdrojového kódu</span><span class="sxs-lookup"><span data-stu-id="69660-131">Modify the source code</span></span>

1. <span data-ttu-id="69660-132">Ve vašem projektu Visual Studio přidejte novou třídu (v tomto příkladu `AssetRollForwardDestination`) a napište kód implementující vlastní cíl pro generované sestavy **Dopředné posunutí dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="69660-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="69660-133">Metoda `new()` je navržena tak, aby získala původní cílový objekt ER a parametr založený na logice aplikace, který určuje vlastní umístění, kam by se měly ukládat generované zprávy.</span><span class="sxs-lookup"><span data-stu-id="69660-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="69660-134">V tomto příkladu je vlastním umístěním název složky místního souborového systému serveru, na kterém je spuštěna služba Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="69660-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="69660-135">Metoda `saveFile()` je určena k uložení vygenerovaného dokumentu do složky místního souborového systému serveru, na kterém je spuštěna služba AOS.</span><span class="sxs-lookup"><span data-stu-id="69660-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="69660-136">Ve vašem projektu Visual Studio přidejte novou třídu (v tomto příkladu `AssetRollForwardDestinationFactory`) a napište kód pro nastavení vlastního cílového objektu pro vytváření, který deleguje vytvoření cíle na výchozí cílový objekt pro vytváření, a kód pro zabalení cíle souboru do vašeho vlastního cíle.</span><span class="sxs-lookup"><span data-stu-id="69660-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="69660-137">Upravte existující třídu `AssetRollForwardService` a zapište kód pro nastavení vlastního cílového objektu pro vytváření, určený pro spouštěč sestavy.</span><span class="sxs-lookup"><span data-stu-id="69660-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="69660-138">Všimněte si, že když je vytvořen vlastní cílový objekt pro vytváření, je předán parametr řízený aplikací, který určuje cílovou složku.</span><span class="sxs-lookup"><span data-stu-id="69660-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="69660-139">Tímto způsobem se tato cílová složka používá k ukládání vygenerovaných souborů.</span><span class="sxs-lookup"><span data-stu-id="69660-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="69660-140">Zkontrolujte, že zadaná složka (v tomto příkladu **c:\\0**) se nachází v místním souborovém systému serveru, na kterém je spuštěna služba AOS.</span><span class="sxs-lookup"><span data-stu-id="69660-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="69660-141">Jinak bude za běhu vyvolána výjimka [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="69660-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
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

4. <span data-ttu-id="69660-142">Znovu sestavte svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="69660-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="69660-143">Opakované spuštění sestavy dopředného posunutí dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="69660-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="69660-144">Přejděte do nabídky **Dlouhodobý majetek** \> **Dotazy a sestavy** \> **Sestavy transakcí** \> **Dopředné posunutí dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="69660-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="69660-145">V poli **Od data** zadejte hodnotu **1/1/2017**.</span><span class="sxs-lookup"><span data-stu-id="69660-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="69660-146">V poli **Do data** zadejte hodnotu **1/31/2017**.</span><span class="sxs-lookup"><span data-stu-id="69660-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="69660-147">V poli **Měna** vyberte hodnotu **Zúčtovací měna**.</span><span class="sxs-lookup"><span data-stu-id="69660-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="69660-148">V poli **Mapování formátu** vyberte **Dopředné posunutí dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="69660-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="69660-149">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="69660-149">Select **OK**.</span></span>
7. <span data-ttu-id="69660-150">Přejděte do složky **C:\\0**, kde najdete vygenerovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="69660-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="69660-151">Protože v tomto příkladu není objekt `originDestination` použit v objektu `AssetRollForwardDestination`, konfigurace pro [cíle](electronic-reporting-destinations.md) formát ER bude za běhu ignorována.</span><span class="sxs-lookup"><span data-stu-id="69660-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69660-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="69660-152">Additional resources</span></span>

- [<span data-ttu-id="69660-153">Místa určení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="69660-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="69660-154">Domovská stránka pro rozšiřitelnost</span><span class="sxs-lookup"><span data-stu-id="69660-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)