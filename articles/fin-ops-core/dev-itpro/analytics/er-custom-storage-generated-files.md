---
title: Určení vlastních umístění úložišť pro vygenerované dokumenty
description: Toto téma vysvětluje, jak rozšířit seznam umístění úložišť pro dokumenty generované formáty elektronického výkaznictví (ER).
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894141"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Určení vlastních umístění úložišť pro vygenerované dokumenty

[!include[banner](../includes/banner.md)]

Aplikační programovací rozhraní (API) rozhraní elektronického výkaznictví umožňuje rozšířit seznam umístění úložišť pro dokumenty, které generují ER formáty. Toto téma vysvětluje, jak přidat vlastní umístění úložiště pro generované dokumenty delegováním úkolu vytváření cílů ER na výchozí cílový objekt pro vytváření a následnou implementací vlastní třídy, která má vlastní logiku cíle.

## <a name="prerequisites"></a>Předpoklady

Nasaďte topologii, která podporuje průběžné sestavování. Další informace naleznete v tématu [Nasazení topologií, které podporují automatizaci průběžného sestavení a testů](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Také musí mít přístup k této topologii pro jednu z následujících rolí.

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

Také musí mít přístup k vývojovému prostředí pro tuto topologii.

Všechny úkoly v tomto tématu lze dokončit ve společnosti **USMF**.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Import formátu ER dopředného posunutí dlouhodobého majetku

Chcete-li vygenerovat dokumenty, u kterých plánujete přidat vlastní umístění úložiště, [importujte](er-download-configurations-global-repo.md) konfiguraci formátu ER **Dopředné posunutí dlouhodobého majetku** do aktuální topologie.

![Stránka úložiště konfigurace](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Spuštění sestavy dopředného posunutí dlouhodobého majetku

1. Přejděte do nabídky **Dlouhodobý majetek** \> **Dotazy a sestavy** \> **Sestavy transakcí** \> **Dopředné posunutí dlouhodobého majetku**.
2. V poli **Od data** zadejte **1/1/2017** (1. leden 2017).
3. V poli **Do data** zadejte **1/31/2017** (31. leden 2017).
4. V poli **Měna** vyberte hodnotu **Zúčtovací měna**.
5. V poli **Mapování formátu** vyberte **Dopředné posunutí dlouhodobého majetku**.
6. Vyberte **OK**.

![Dialogové okno modulu runtime pro sestavu dopředného posunutí dlouhodobého majetku](./media/er-custom-storage-generated-files-runtime-dialog.png)

v aplikaci Microsoft Excel zkontrolujte odchozí dokument, který je generován a je k dispozici ke stažení. Toto chování je [výchozí](electronic-reporting-destinations.md#default-behavior) pro formát ER, který nemá konfigurovány žádné [cíle](electronic-reporting-destinations.md) a běží v interaktivním režimu.

## <a name="review-the-source-code"></a>Kontrola zdrojového kódu

Zkontrolujte kód metody `generateReportByGER()` třídy `AssetRollForwardService`. Všimněte si, že k volání architektury ER a generování sestavy **Dopředné posunutí dlouhodobého majetku** se používá metoda `Run()`.

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

## <a name="modify-the-source-code"></a>Úprava zdrojového kódu

1. Ve vašem projektu Visual Studio přidejte novou třídu (v tomto příkladu `AssetRollForwardDestination`) a napište kód implementující vlastní cíl pro generované sestavy **Dopředné posunutí dlouhodobého majetku**.

    - Metoda `new()` je navržena tak, aby získala původní cílový objekt ER a parametr založený na logice aplikace, který určuje vlastní umístění, kam by se měly ukládat generované zprávy. V tomto příkladu je vlastním umístěním název složky místního souborového systému serveru, na kterém je spuštěna služba Application Object Server (AOS).
    - Metoda `saveFile()` je určena k uložení vygenerovaného dokumentu do složky místního souborového systému serveru, na kterém je spuštěna služba AOS.

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

2. Ve vašem projektu Visual Studio přidejte novou třídu (v tomto příkladu `AssetRollForwardDestinationFactory`) a napište kód pro nastavení vlastního cílového objektu pro vytváření, který deleguje vytvoření cíle na výchozí cílový objekt pro vytváření, a kód pro zabalení cíle souboru do vašeho vlastního cíle.

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

3. Upravte existující třídu `AssetRollForwardService` a zapište kód pro nastavení vlastního cílového objektu pro vytváření, určený pro spouštěč sestavy. Všimněte si, že když je vytvořen vlastní cílový objekt pro vytváření, je předán parametr řízený aplikací, který určuje cílovou složku. Tímto způsobem se tato cílová složka používá k ukládání vygenerovaných souborů.

    > [!NOTE] 
    > Zkontrolujte, že zadaná složka (v tomto příkladu **c:\\0**) se nachází v místním souborovém systému serveru, na kterém je spuštěna služba AOS. Jinak bude za běhu vyvolána výjimka [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).

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

4. Znovu sestavte svůj projekt.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Opakované spuštění sestavy dopředného posunutí dlouhodobého majetku

1. Přejděte do nabídky **Dlouhodobý majetek** \> **Dotazy a sestavy** \> **Sestavy transakcí** \> **Dopředné posunutí dlouhodobého majetku**.
2. V poli **Od data** zadejte hodnotu **1/1/2017**.
3. V poli **Do data** zadejte hodnotu **1/31/2017**.
4. V poli **Měna** vyberte hodnotu **Zúčtovací měna**.
5. V poli **Mapování formátu** vyberte **Dopředné posunutí dlouhodobého majetku**.
6. Vyberte **OK**.
7. Přejděte do složky **C:\\0**, kde najdete vygenerovaný soubor.

> [!NOTE]
> Protože v tomto příkladu není objekt `originDestination` použit v objektu `AssetRollForwardDestination`, konfigurace pro [cíle](electronic-reporting-destinations.md) formát ER bude za běhu ignorována.

## <a name="additional-resources"></a>Další prostředky

- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Domovská stránka pro rozšiřitelnost](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]