---
title: Nastavení alternativního datového toku pro doporučení
description: Tento článek popisuje, jak nakonfigurovat prostředí pomocí alternativního toku dat k poskytování dat službě doporučení.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460157"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Nastavení alternativního datového toku pro doporučení

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat prostředí pomocí alternativního toku dat k poskytování dat službě doporučení.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Porovnání hotových toků dat s alternativním tokem dat

Následující obrázek znázorňuje hotový tok dat v prostředí.

![Hotový tok dat v prostředí](media/reco-out-of-the-box-dataflow-2.png)

Následující obrázek znázorňuje alternativní tok dat, kde je dávková úloha synchronizace úložiště entit nahrazena alternativními kroky toku dat.

![Alternativní tok dat v prostředí](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Předpoklady

- Tento článek předpokládá, že jste již aktivovali službu doporučení pro vaše prostředí. Další informace viz [Aktivace doporučení produktů](enable-product-recommendations.md).
- Když pracujete se soubory a složkami v účtu Microsoft Azure Data Lake Storage:

    - Můžete použít buď rozhraní webového portálu Azure, nebo aplikaci Azure Storage Explorer.
    - Výchozí body pro práci se soubory a složkami jsou v kontejneru **dynamics365-financeandoperations**, který se nachází pod složkou pojmenovanou tak, aby odpovídala adrese URL vašeho prostředí.
    - Pokud je název vašeho prostředí sandbox **MyUAT**, základní adresa URL prostředí bude `myuat.sandbox.operations.dynamics.com`.
    - Pokud je ke stejnému účtu úložiště připojeno více než jedno prostředí, každé prostředí bude mít svou vlastní kořenovou složku.

## <a name="prerequisites"></a>Předpoklady

Než budete moci implementovat alternativní přístup datového toku, musí být splněny následující předpoklady.

### <a name="set-up-microsoft-power-platform"></a>Nastavit systém Microsoft Power Platform

K nastavení Microsoft Power Platform postupujte podle pokynů v části [Aktivace integrace Microsoft Power Platform](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Instalace doplňku Export do Data Lake

Chcete-li nainstalovat doplněk Export do Data Lake, postupujte podle pokynů v části [Instalace doplňku Export do Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Poznamenejte si konfigurační hodnoty, protože je budete potřebovat pro některé z následujících kroků.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Konfigurace tabulek pro export v Dynamics 365

Synchronizace tabulek z Dynamics 365 do Azure Data Lake Storage je spravován na stránce **Export do Data Lake**. Protože tato stránka aktuálně nemá položku nabídky, mohou ji otevřít pouze uživatelé v roli zabezpečení **Správce systému**.

Chcete-li nakonfigurovat tabulky pro export v Dynamics 365, postupujte takto.

1. Chcete-li otevřít stránku **Export do Data Lake**, přidejte řetězec `?mi=DataFeedsDefinitionWorkspace` k základní adrese URL prostředí, jak ukazuje následující příklad:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Na stránce **Export do Data Lake** zkopírujte tabulky, které jsou uvedeny v části [Seznam tabulek datové krychle RetailSales](#list-of-retailsales-cube-tables) tohoto článku.
1. Ve sloupci **Název systému** rozbalte seznam možností filtrování.
1. Jako typ filtru vyberte **je jeden z**. Poté umístěte kurzor do textového pole a vložte seznam tabulek, které jste zkopírovali ze stránky **Export do Data Lake**.
1. V dolní části seznamu možností filtru vyberte **Aplikovat**.
1. Vyberte všechny řádky v mřížce a poté vyberte **Aktivovat**.

> [!NOTE]
> Než přejdete k dalšímu kroku, musí být všechny řádky aktualizovány na stav **Spuštěné**. Odstraňte a vyřešte případné chyby podle potřeby.

### <a name="create-a-synapse-workspace"></a>Vytvoření pracovního prostoru Synapse

Chcete-li vytvořit pracovní prostor Synapse, pokud jej ještě nemáte, postupujte podle pokynů v části [Rychlý start: Vytvoření pracovního prostoru Synapse](/azure/synapse-analytics/quickstart-create-workspace).

Chcete-li mít své prostředky Azure organizované, doporučujeme dát účet Data Lake Storage a pracovní prostor Synapse dohromady do skupiny prostředků v Azure. Můžete využít účet úložiště, který jste vytvořili při instalaci doplňku Export do Data Lake.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Vytvoření databáze v Synapse pro zpracování dat doporučení

Pomocí konzolové aplikace nástroje Common Data Model (CDMUtil_ConsoleApp) vytvořte databázi ve svém pracovním prostoru Synapse a naplňte ji z tabulek Common Data Model v Data Lake Storage. Doporučujeme použít nástroj Common Data Model s vaší databází ve vývojovém prostředí v případě, že existují nějaká rozšíření.

> [!NOTE]
> Následující kroky předpokládají, že do datové krychle RetailSales nejsou přidávána žádná data rozšíření.

K vytvoření databáze v Synopse postupujte následovně.

1. Přejděte na [GitHub Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) a postupujte podle pokynů ke stažení souboru **CDMUtilConsoleApp.zip**.
1. Extrahujte soubor zip do místní složky.
1. Otevřete soubor **CDMUtil_ConsoleApp.dll.config** soubor v textovém editoru a aktualizujte následující hodnoty:

    1. Nastavte hodnotu **ID tenanta** – (ID tenanta Azure).
    1. Nastavte hodnotu **Přístupový klíč** (přístupový klíč pro účet Data Lake Storage).

        1. V portálu Azure otevřete účet úložiště.
        1. V nabídce na levé straně stránky vyberte **Přístupové klíče**.
        1. V horní části stránky vyberte **Zobrazit klíče**.
        1. Vyberte tlačítko kopírování pro jedno ze dvou polí klíčů a potom vložte hodnotu do dvojitých uvozovek v konfiguračním souboru.

    1. Nastavte hodnotu **ManifestURL** na adresu URL vašeho souboru **Tables.manifest.cdm.json** v Azure Data Lake Storage. Chcete-li získat adresu URL, přejděte do souboru na Azure Portal, vyberte tři tečky (**...**) na pravé straně pohledu a poté vyberte **Vlastnosti**. Adresa URL je první vlastností, která je zobrazena na kartě **Přehled**.
    1. Nastavte hodnotu **TargetDbConnectionString** na připojovací řetězec pro vestavěný bezserverový fond SQL vašeho pracovního prostoru Synapse.

        1. Na pracovním prostoru Synapse vyberte kartu **Spravovat**.
        1. V podnabídce vyberte **Fondy SQL**.
        1. Vyberte název **Vestavěný** pro zobrazení vlastností fondu.
        1. V dialogovém okně vlastností vyberte typ připojení ADO.NET, které chcete použít. Potom zkopírujte hodnotu připojovacího řetězce a vložte ji mezi dvojité uvozovky v konfiguračním souboru.

        > [!NOTE]
        > Musíte mít oprávnění k vytváření databází. Pro snadné použití možná budete chtít použít vestavěný účet správce **sqladminuser**.

    1. Zrušte zakomentování uzlu **ProcessEntities** a nastavte jeho hodnotu na **true** (například `<add key="ProcessEntities" value ="true"/>`).

1. Uložte a zavřete soubor **CDMUtil_ConsoleApp.dll.config**.
1. Zkopírujte soubor **EntityList.json** do adresáře **/Manifest**.
1. V okně příkazového řádku spusťte **cdmutil_consoleapp.exe**.

> [!NOTE]
> Při kontrole výstupu by mělo být existovat 35 entit/pohledů, alespoň 75 tabulek a žádné chyby.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Připravte adresář Agregovaná měření Data Lake RetailSales

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Zálohujte svá aktuální data datové krychle RetailSales z Data Lake Storage

Nejjednodušší způsob, jak zálohovat aktuální data datové krychle RetailSales, je přejmenovat adresář **RetailSales** adresář v Data Lake Storage na **RetailSales-backup** nebo něco podobného. Tato metoda zachovává existující data pro případ, že by bylo později nutné řešení problémů.

Složku datové krychle **/RetailSales** naleznete v následujícím umístění:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Vytvoření nové složky RetailSales a nahrání souboru modelu

Chcete-li vytvořit nový adresář **RetailSales** a nahrát soubor **model.json** do Data Lake Storage, postupujte takto.

1. Vytvořte nový prázdný adresář na stejné úrovni jako předchozí adresář a pojmenujte ho **RetailSales**.
1. Nahrajte soubor **model.json** do nového adresáře.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Vytvoření kanálu pro kopírování dat datové krychle RetailSales

Kanál bude číst pohledy datové krychle RetailSales a exportovat data do souborů .csv v Data Lake Storage.

Pro vytvoření kanálu pro kopírování dat datové krychle RetailSales postupujte následovně.

1. Na pracovním prostoru Synapse vyberte kartu **Integrovat**.
1. Vyberte znaménko plus (**+**) a poté vyberte **Importovat ze šablony kanálu**.
1. Stáhněte a poté vyberte [soubor ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Vyberte propojenou službu databáze SQL.
1. Vyberte propojenou službu účtu úložiště.
1. Otevřete nástroj **Kopírování dat** a změňte vlastnost **Folder path** na **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Zkouška vykonávání kanálu

Doporučujeme testovat kanál pomocí pouze jednoho zobrazení. Pohled **RetailSales_RetailMediaTemplateView** funguje dobře, protože obvykle obsahuje méně než 10 řádků.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Naplánování běhu kanálu podle opakujícího se plánu

Při každém spuštění kanálu dochází ke spotřebě Azure. Doporučujeme naplánovat spouštění v intervalech 48 hodin nebo déle. Pokud musíte okamžitě synchronizovat data, můžete kanál vždy spustit ručně. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Seznam tabulek pro synchronizaci z Dynamics 365 do Data Lake Storage

Následující seznam tabulek je podmnožinou všech tabulek, které jsou vyžadovány pro celou datovou krychli RetailSales. Služba doporučení používá pouze 15 zobrazení v datové krychli RetailSales a podle toho byl filtrován seznam požadovaných tabulek.

### <a name="list-of-retailsales-cube-tables"></a>Seznam tabulek datových krychlí RetailSales

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Zobrazení seznamu parametrů, který má být předán do kanálu Synapse

Následující seznam oddělený čárkami obsahuje pohledy datové krychle RetailSales, na kterých kanál provede operaci „select“. Výsledky pak zkopíruje do úložiště Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Parametr kanálu musí být seznam názvů zobrazení, které jsou odděleny jednou čárkou. Nesmí obsahovat žádné mezery ani odřádkování.

## <a name="environment-specific-fixes"></a>Opravy specifické pro prostředí

### <a name="retailchannelview-fix"></a>Oprava RETAILCHANNELVIEW

Pohled **RETAILCHANNELVIEW** obsahuje pevně zakódované celé číslo, které představuje organizaci typu „maloobchodní kanál“. Skutečná hodnota typu se může měnit z prostředí na prostředí nebo z tenanta na tenanta.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Chcete-li aktualizovat pevně zapsané celé číslo, postupujte následujícím způsobem.

1. V Dynamics 365 vyhledejte hodnotu **ChannelID** pro váš online kanál.
1. V instanci SQL Server Management Studio (SSMS), která je připojena k databázi Synapse, spusťte následující dotaz.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Zkopírujte hodnotu z prvního sloupce (**INSTANCERELATIONTYPE**) a vložte ji do definice pohledu.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="pipeline-task-fails"></a>Úloha kanálu se nezdaří

Mělo by existovat 15 provedení úloh kanálu úlohy **CopyData**. Pokud se jakékoli provedení nezdaří, musíte ověřit, že existují všechny závislé objekty SQL a že jsou spuštěny dotazy. Ke všem závislostem se nejsnáze dostanete pomocí SSMS pro připojení k databázi. Poté můžete podržet (nebo kliknout pravým tlačítkem na) zobrazení a vybrat **Vygenerovat CREATE jako do nového okna**.

Chybová zpráva může obsahovat následující text:

- Chyba: Na straně zdroje došlo k selhání
- Chyba při zpracování externího souboru: „Maximální počet chyb“.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Příklad

V tomto příkladu se úloha **RetailSales_RetailProductCategory** nezdaří a zobrazí se chyba „Maximální počet chyb“.

Tuto chybu opravíte pomocí následujícího postupu:

1. Otevřete soubor **EntityList.json** v textovém editoru (např. Visual Studio Code).
1. Najděte definici pohledu pro **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Tento pohled závisí pouze na jednom dalším pohledu: **RetailProductCategoryView** _. Najděte definici pohledu pro _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Tento pohled závisí na třech dalších pohledech: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** a **RETAILCATEGORYEXPANDED**. Najděte definici každého z těchto pohledů a vypište jeho závislosti. Pokračujte, dokud nenajdete všechny závislé pohledy.

    Zde je celý seznam v pořadí stromu závislostí. Musí být ověřeno třináct pohledů.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. V Excelu vytvořte následujících 13 příkazů **select count(\*) from \<view_name\>**. Spusťte tyto příkazy v SSMS a odešlete výsledky do textu. Poté procházejte výsledky a zjistěte, zda některý z pohledů selhal. Počáteční chyba naznačuje, že alespoň jeden pohled selže.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Jedním ze způsobů, jak ověřit to, na co se díváte, je vytvořit pohled závislý na kořenech pro generování definice pohledu v SSMS. Potom ověřte, že existuje sloupec souboru Azure Data Lake s názvem **r.filepath**. Přítomnost tohoto sloupce bude znamenat, že zobrazení, které kontrolujete, čte data z Data Lake Storage.

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
