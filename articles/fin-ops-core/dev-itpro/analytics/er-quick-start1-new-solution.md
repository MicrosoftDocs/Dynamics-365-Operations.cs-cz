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
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35db2eb3e0da91207f08d16b8fb1bfa6a6bb8607
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345953"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Navrhněte nové řešení ER pro tisk vlastní sestavy

[!include[banner](../includes/banner.md)]

Následující kroky vysvětlují, jak může uživatel v roli administrátora systému, vývojáře elektronických zpráv nebo funkčního konzultanta pro elektronické vykazování konfigurovat parametry rámce ER, navrhovat požadované konfigurace ER nového řešení ER pro přístup k datům konkrétní obchodní domény, a vygenerovat vlastní přehled ve formátu Microsoft Office. Tyto kroky lze provést v rámci společnosti **USMF**.

- [Konfigurace architektury ER](#ConfigureFramework)

    - [Konfigurace parametrů ER](#ConfigureParameters)
    - [Aktivace poskytovatele konfigurace ER](#ActivateProvider)

        - [Kontrola seznamu poskytovatelů konfigurace ER](#ReviewProvidersList)
        - [Přidání nového poskytovatele konfigurace ER](#AddProvider)
        - [Aktivace poskytovatele konfigurace ER](#ActivateAddedProvider)

- [Návrh datového modelu specifického pro doménu](#DesignModel)

    - [Import nové konfigurace datového modelu](#ImportDataModel)
    - [Vytvoření nové konfigurace datového modelu](#DesignDataModel)

        - [Pojmenování datového modelu](#NameDataModel)
        - [Přidání pole datového modelu](#FieldsEntry)
        - [Dokončení návrhu datového modelu](#CompleteDataModel)

- [Návrh mapování modelu pro konfigurovaný datový model](#DesignMapping)

    - [Import nové konfigurace mapového modelu](#ImportModelMapping)
    - [Vytvoření nové konfigurace mapování modelu](#CreateModelMapping)

        - [Návrh nového komponentu mapování modelu](#DesignMappingComponent)
        - [Přidání zdroje dat pro přístup k aplikačním tabulkám](#AddMmDataSource1)
        - [Přidání zdroje dat pro přístup k výčtům aplikací](#AddMmDataSource2)
        - [Přidání štítků ER a vygenerování sestavy ve specifikovaném jazyce](#AddMmLabels)
        - [Přidání zdroje dat pro transformaci výsledků porovnání hodnot výčtu k textové hodnotě](#AddMmDataSource3)
        - [Navázání zdroje dat na pole zdrojů dat](#AddMmBindings1)
        - [Dokončení návrhu mapování modelu](#CompleteModelMapping)

- [Navrhněte šablonu pro vlastní sestavu](#DesignReportTemplate)
- [Návrh formátu](#DesignFormat)

    - [Import navrženého formátu konfigurace](#FormatImport)
    - [Vytvoření nové konfigurace formátu](#FormatCreate)

        - [Import šablony sestavy](#ImportReportTemplate)
        - [Konfigurace formátu](#ConfigureFormat)
        - [Definice datové vazby pro název sestavy](#DefineFormatBindings)
        - [Kontrola zdrojových data modelu](#ReviewModelDataSource)
        - [Vázání prvků formátu na pole zdroje dat](#BindFormatElements)

    - [Spuštění navrženého formátu z ER](#RunFormatFromER)

- [Vylaďte navržený formát](#TuneFormat)

    - [Upravte formát a změňte název generovaného dokumentu](#ModifyToChangeName)
    - [Upravte formát a změňte pořadí otázek](#ModifyToOrder)
    - [Spuštění upraveného formátu z ER](#RunFormatFromER2)
    - [Dokončete návrh formátu](#CompleteFormat)

- [Vytvořte artefakty aplikace a pojmenujte navrženou sestavu](#DevelopCustomCode)

    - [Úprava zdrojového kódu](#ModifySourceCode)

        - [Přidejte třídu datového kontraktu](#DataContractClass)
        - [Přidejte třídu tvůrce uživatelského rozhraní](#UIBuilderClass)
        - [Přidejte třídu poskyovatele dat](#DataProviderClass)
        - [Přidejte soubor štítků](#LabelsFile)
        - [Přidejte třídu služby sestav](#ServiceClass)
        - [Přidejte třídu kontrolera sestav](#ControllerClass)
        - [Přidejte položku nabídky](#MenuItem)
        - [Přidejte položku nabídky k nabídce](#Menu)
        - [Sestavte Visual Studio projekt](#BuildVSProject)

    - [Spusťte formát z aplikace](#RunFormatFromApp)

- [Vylaďte navržené řešení ER](#TuneSolution)

    - [Úprava mapování modelu](#ModifyModelMapping)

        - [Přidání zdroje dat pro přístup k objektu kontraktu dat](#AddDataSource1)
        - [Přidejte zdroj dat pro přístup k záznamům mapování formátu ER](#AddDataSource2)
        - [Přidejte zdroj dat pro přístup k záznam mapování běžícího formátu ER](#AddDataSource3)
        - [Zadejte název datového modelu běžícího formátu ER](#AddBinding)
        - [Dokončení návrhu mapování modelu](#CompleteModelMapping2)

    - [Změna formátu](#ModifyFormat)

        - [Přidat nový prvek formátu](#AddFormatElement)
        - [Vázání přidaného prvku formátu](#BindAddedFormatElement)
        - [Dokončete návrh formátu](#CompleteFormat2)

    - [Spusťte formát z aplikace](#RunFormatFromApp2)
    - [Spusťte formát z ER](#RunFormatFromER3)
    - [Konfigurace cílového formátu pro náhled na obrazovce](#ConfigureDestination)
    - [Spusťte formát z aplikace a zobrazte jej jako dokument PDF](#RunFormatFromApp3)

- [Další prostředky](#References)

V tomto příkladu vytvoříte nové řešení ER pro modul [Dotazník](../../../human-resources/hr-learning-questionnaires.md). Toto nové řešení ER vám umožňuje navrhnout sestavu pomocí listu Microsoft Excel jako šablony. Poté můžete vygenerovat **Dotazník** sestavu ve formátu Excel nebo PDF, kromě generování existující zprávy SQL Server Reporting Services (SSRS). Novou sestavu můžete také na požádání upravit později. Není nutné žádné kódování.

1. Chcete-li spustit stávající sestavu, přejděte na **Dotazník** \> **Design** \> **Sestava dotazníků**.

    ![Výběrem položky nabídky Přehled dotazníků v modulu Dotazník spustíte existující sestavu SSRS.](./media/er-quick-start1-application-menu-origin.png)

2. V dialogovém okně **Sestava dotazníků** zadejte kritéria výběru. Použijte filtr tak, aby přehled obsahoval pouze **SBCCrsExam** dotazník.

    ![V dialogovém okně Sestava dotazníků zadejte kritéria výběru.](./media/er-quick-start1-ssrs-report-dialog.png)

Následující obrázek ukazuje generovanou verzi zprávy SSRS pro dotazník **SBCCrsExam**.

![Generovaná SSRS sestava.](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Konfigurace rámce ER

Jako uživatel v roli vývojáře elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER, abyste mohli začít používat rámec ER k navrhovánínového ER řešení.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Konfigurace parametrů ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. V pracovním prostoru **Elektronické sestavy** vyberte **Parametry elektronického vykazování**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.
4. Na kartě **Přílohy** natavte následující parametry:

    - V poli **Konfigurace** vyberte pro společnost **USMF** typ **Soubor**.
    - V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.

Další informace o parametrech ER najdete v tématu [Konfigurace rámce ER](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Aktivace poskytovatele konfigurace ER

U každé označené konfigurace ER je vyznačen jako vlastník poskytovatel konfigurace ER. Než začnete přidávat nebo upravovat konfigurace ER, musíte proto aktivovat poskytovatele konfigurace ER v pracovním prostoru **Elektronické výkaznictví**.

> [!NOTE]
> Pouze vlastník konfigurace ER může konfiguraci upravovat. Konfiguraci ER proto můžete upravovat teprve poté, co je příslušná konfigurace ER aktivována v pracovním prostoru **Elektronické výkaznictví**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Kontrola seznamu poskytovatelů konfigurace ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Poskytovatelé konfigurace**.
3. Na stránce **Poskytovatelé konfigurace** má záznam každé konfigurace jedinečný název a adresu URL. Zkontrolujte obsah této stránky. Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#ActivateProvider), přeskočte.

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Přidání nového poskytovatele konfigurace ER

1. Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.
2. Do pole **Název** zadejte **Litware, Inc.**
3. Do pole **Internetová adresa** zadejte `https://www.litware.com`.
4. Zvolte **Uložit**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Aktivace poskytovatele konfigurace ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. V **Elektronickém výkaznictí** vyberte **Litware, Inc.** pro vašeho poskytovatele konfigurace.
3. Vyberte **Nastavit jako aktivní**.

Další informace o poskytovatelích konfigurací ER naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Návrh datového modelu specifického pro doménu

Musíte vytvořit novou konfiguraci ER obsahující součást [datový model](general-electronic-reporting.md#data-model-and-model-mapping-components) pro obchodní doménu **Dotazník**. Tento datový model bude později použit jako zdroj dat, když navrhujete formát ER pro generování sestavy **Dotazník**.

Dokončením kroků v části [Importujte novou konfiguraci datového modelu](#ImportDataModel) můžete importovat požadovanou konfiguraci datového modelu z poskytnutého souboru XML. Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace datového modelu](#DesignDataModel), chcete-li navrhnout tento datový model od začátku.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Import nové konfigurace datového modelu

1. Stáhněte si soubor [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires model.version.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace datového modelu](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Vytvoření nové konfigurace datového modelu

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
3. Vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně do pole **Název** zadejte **Model dotazníku**.
5. Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Pojmenování datového modelu

1. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.
2. Vyberte možnost **Návrhář**.
3. Na stránce **Návrhář datového modelu** v pevné záložce **Obecné**, do pole **Název** zadejte <a name="DataModeName"></a>**Dotazníky**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Přidání nového pole datového modelu

1. Na stránce **Návrhář datového modelu** zvolte **Nový**.
2. V rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Vyberte **Kořen modelu** jako typ nového uzlu.
    2. Do pole **Název** zadejte řetězec <a name="RootDefinitionName"></a>**Kořen**.
    3. Kliknutím na **Přidat** přidáte nový uzel.

    Tento kořenový popisovač se použije k poskytování dat pro sestavu **Dotazník**. Jeden datový model může mít více popisovačů. Každý popisovač může být určen pro jeden formát ER pro identifikaci dat, která jsou vyžadována pro generování sestavy.

3. Znovu zvolte **Nový** a poté v rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Vyberte **Podřízený aktivního uzlu** jako typ nového uzlu.
    2. Do pole **Název** zadejte **CompanyName**.
    3. V poli **Typ položky** vyberte **Řetězec**.
    4. Kliknutím na **Přidat** přidáte nové pole.

    Toto pole je vyžadováno pro předání názvu aktuální společnosti do sestavy ER, která používá tento datový model jako zdroj dat.

4. Znovu zvolte **Nový** a poté v rozevíracím dialogovém okně pro přidání uzlu datového modelu postupujte takto:

    1. Vyberte **Podřízený aktivního uzlu** jako typ nového uzlu.
    2. Do pole **Název** zadejte **Dotazník**.
    3. V poli **Typ položky** vyberte **Seznam záznamů**.
    4. Kliknutím na **Přidat** přidáte nové pole.

    Toto pole bude použito pro předání seznamu dotazníků do sestavy ER, která používá tento datový model jako zdroj dat.

5. Vyberte uzel **Dotazník**.
6. Stejným způsobem pokračujte v přidávání povinných polí upravitelného datového modelu, dokud nedokončíte následující strukturu datového modelu.

    | Cesta pole                                                    | Datový typ   | Označení pole / vrácená hodnota |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Kořen                                                          |             | Referenční bod pro vyžádání údajů z dotazníku. |
    | Root\\CompanyName                                             | Řetězec      | Název aktuální společnosti. |
    | Root\\ExecutionContext                                        | Záznam      | Podrobnosti o spuštění formátu. |
    | Root\\ExecutionContext\\FormatName                            | Řetězec      | Název právě spuštěného formátu ER. |
    | Root\\Questionnaire                                           | Seznam záznamů | Seznam dotazníků |
    | Root\\Questionnaire\\Active                                   | Řetězec      | Stav aktuálního dotazníku. |
    | Root\\Questionnaire\\Code                                     | Řetězec      | Kód aktuálního dotazníku. |
    | Root\\Questionnaire\\Description                              | Řetězec      | Popis aktuálního dotazníku. |
    | Root\\Questionnaire\\QuestionnaireType                        | Řetězec      | Typ aktuálního dotazníku. |
    | Root\\Questionnaire\\QuestionOrder                            | Řetězec      | Číselné pořadí aktuálního dotazníku. |
    | Root\\Questionnaire\\ResultsGroup                             | Záznam      | Výsledné parametry aktuálního dotazníku. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | Řetězec      | Identifikační kód aktuální skupiny výsledků. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | Řetězec      | Popis aktuálnískupiny výsledků. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Reálný        | Maximální počet bodů, které lze získat. |
    | Root\\Questionnaire\\Question                                 | Seznam záznamů | Seznam otázek pro aktuální dotazník. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Celé číslo     | Pořadové číslo aktuální kolekce odpovědí. |
    | Root\\Questionnaire\\Question\\Id                             | Řetězec      | Identifikační kód aktuální otázky. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | Řetězec      | Příznak, který označuje, zda je třeba odpovědět na aktuální otázku. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | Řetězec      | Příznak, který označuje, zda je aktuální otázka primární. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Celé číslo     | Pořadové číslo aktuální otázky. |
    | Root\\Questionnaire\\Question\\Text                           | Řetězec      | Text aktuální otázky. |
    | Root\\Questionnaire\\Question\\Answer                         | Seznam záznamů | Seznam odpovědí pro aktuální otázku. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | Řetězec      | Příznak, který označuje, zda je aktuální odpověď správná. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Reálný        | Body, které získáte, když je vybrána aktuální odpověď. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Celé číslo     | Pořadové číslo aktuální odpovědi. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | Řetězec      | Text aktuální odpovědi. |

    Následující obrázek ukazuje dokončený upravitelný datový model na stránce **Návrhář datového modelu**.

    ![Konfigurovaný datový model v návrháři datového modelu ER.](./media/er-quick-start1-model2.png)

7. Uložte změny.
8. Zavřete stránku **Návrhář datového modelu**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Dokončení návrhu datového modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.
3. Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
4. Vyberte **Změnit stav** \> **Dokončeno**.

Stav verze 1 této konfigurace se změní z **Návrh** na **Dokončeno**. Verzi 1 již nelze změnit. Tato verze obsahuje konfigurovaný datový model a lze ji použít jako základ pro další konfigurace ER. Verze 2 této konfigurace je vytvořena a má stav **Návrh**. Tuto verzi můžete upravit a tak upravit datový model **Dotazník**.

![Verze konfigurovatelné konfigurace na stránce Konfigurace.](./media/er-quick-start1-model-configuration.png)

Další informace o verzích pro konfigurace ER viz [Přehled elektronického výkaznictví (ER)](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Konfigurovaný datový model je vaše abstraktní reprezentace obchodní domény **Dotazník** a neobsahuje žádné vztahy k artefaktům, které jsou specifické pro službu Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Návrh mapování modelu pro konfigurovaný datový model

Jako uživatel v roli Electronic Reporting Developer musíte vytvořit novou konfiguraci ER, která obsahuje [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) součást pro **Dotazník** datový model. Protože tato komponenta implementuje nakonfigurovaný datový model pro Finance, je specifická pro Finance. Komponentu mapování modelu musíte nakonfigurovat, abyste určili aplikační objekty, které musí být použity k vyplnění nakonfigurovaného datového modelu aplikačními daty za běhu. K dokončení tohoto úkolu si musíte být vědomi podrobností o implementaci datové struktury systému **Dotazník** obchodní domény ve financích.

Dokončením kroků v [Importujte novou konfiguraci mapování](#ImportModelMapping) datového modelu v další části můžete importovat požadovanou konfiguraci mapování z poskytnutého souboru XML. Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace mapování modelu](#CreateModelMapping), chcete-li navrhnout tento model mapování od začátku.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Import nové konfigurace mapového modelu

1. Stáhněte si soubor [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires mapping.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace mapování modelu](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Vytvoření nové konfigurace mapování modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.
3. Vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně proveďte následující kroky:

    1. V poli **Nový** vyberte **Mapování modelu založené na datovém modelu pro dotazníky**'.
    2. Do pole **Název** zadejte **Mapování dotazníků**'.
    3. V poli **Definice datového modelu** vyberte definici **Kořen**.
    4. Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Návrh nového komponentu mapování modelu

1. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Mapování dotazníku**.
2. Výběrem možnosti **Návrhář** otevřete seznam mapování.
3. Vyberte mapování **Mapování dotazníků**, které bylo automaticky přidáno pro definici **Kořen**
4. Vybrat **Návrhář** k zahájení konfigurace vybraného mapování.

Nové mapování je automaticky přidáno pro definici **Kořen**. Toto mapování má směr **K modelu**. Toto mapování lze proto použít k vyplnění datového modelu požadovanými daty.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Přidání zdroje dat pro přístup k aplikačním tabulkám

Pro přístup k aplikačním tabulkám, které obsahují podrobnosti dotazníku, musíte nakonfigurovat zdroje dat.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Záznamy tabulky**.
2. Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMCollection, kde každý záznam představuje jeden dotazník:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V dialogovém okně do pole **Název** zadejte **Dotazník**.
    3. Do pole **Tabulka** zadejte **KMCollection**.
    4. Nastavte možnost **Zeptat se na dotaz** na **Ano**. Poté budete moci určit možnosti [filtrování](../../fin-ops/get-started/advanced-filtering-query-options.md) pro tuto tabulku v dialogovém okně systémového dotazu za běhu.
    5. Vyberte **OK** pro přidání nového zdroje dat.

3. V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulkové záznamy**.
4. Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMQuestion, kde každý záznam představuje jednu otázku v dotazníku:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V dialogovém okně do pole **Název** zadejte **Otázka**.
    3. Do pole **Tabulka** zadejte **KMQuestion**.
    4. Vyberte **OK** pro přidání nového zdroje dat.

5. V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulkové záznamy**.
6. Přidejte nový zdroj dat, který bude použit pro přístup do tabulky KMAnswer, kde každý záznam představuje jednu odpověď na otázku v dotazníku:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. Do pole **Název** zadejte **Odpověď**.
    3. Do pole **Tabulka** zadejte **KMAnswer**.
    4. Vyberte **OK** pro přidání nového zdroje dat.

7. V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.
8. Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu tabulky KMQuestionResultGroup z každého záznamu nadřazené tabulky KMCollection:

    1. V podokně **Zdroje dat** vyberte **Dotazník**.
    2. Vyberte **přidat**.
    3. V dialogovém okně do pole **Název** zadejte **\$ResultGroup**.
    4. Vyberte možnost **Upravit vzorec**.
    5. V [Editoru vzorců ER](general-electronic-reporting-formula-designer.md), v poli **Vzorec**, zadejte **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** k použití vzájemných vztahů mezi tabulkami KMCollection a KMQQuestionesultGroup typu [cesta](er-formula-language.md#Paths).
    6. Zvolte **Uložit** a pak zavřete editor vzorců.
    7. Vyberte **OK** pro přidání nového počítaného pole.

9. V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.
10. Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu dotazů tabulky KMQuestion z každého záznamu nadřazené tabulky KMCollectionQuestion:

    1. V podokně **Zdroje dat** vyberte **Dotazník**.
    2. Rozbalte uzel **\<Vztahy**, který obsahuje vzájemné vztahy mezi dvěma členy tabulky KMCollection.
    3. Vyberte související tabulku **KMCollectionQuestion** a vyberte **Přidat**.
    4. V dialogovém okně do pole **Název** zadejte **\$Otázka**.
    5. Vyberte možnost **Upravit vzorec**.
    6. V editoru vzorců v poli **Vzorec** zadejte **FIRSTORNULL(FILTER (Question, Question.kmQuestionId = \@.kmQuestionId))** k vrácení příslušných záznamů otázek z tabulky KMQuestion.
    7. Zvolte **Uložit** a pak zavřete editor vzorců.
    8. Vyberte **OK** pro přidání nového počítaného pole.

11. V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.
12. Přidejte nové vypočtené pole, které bude použito pro přístup k záznamu odpovědí tabulky KMAnswer z každého záznamu nadřazené tabulky KMQuestion:

    1. V podokně **Zdroje dat** vyberte **Dotazník.\<Relations.KMCollectionQuestion.\$Question** a poté vyberte **Přidat**.
    2. V dialogovém okně do pole **Název** zadejte **\$Odpověď**.
    3. Vyberte možnost **Upravit vzorec**.
    4. V editoru vzorců v poli **Vzorec** zadejte **FIRSTORNULL(FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId))** k vrácení příslušných záznamů otázek z tabulky KMAnswer.
    5. Zvolte **Uložit** a pak zavřete editor vzorců.
    6. Vyberte **OK** pro přidání nového počítaného pole.

13. V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Tabulka**.
14. Přidejte nový zdroj dat, který bude použit pro přístup k metodám tabulky CompanyInfo. Všimněte si, že metoda **find()** této tabulky vrací záznam, který představuje společnost aktuální instance Finance, kterou se toto mapování nazývá v kontextu.

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V dialogovém okně do pole **Název** zadejte **CompanyInfo**.
    3. Do pole **Tabulka** zadejte **CompanyInfo**.
    4. Vyberte **OK** pro přidání nového zdroje dat.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Přidání zdroje dat pro přístup k výčtům aplikací

Pro přístup k výčtu aplikací musíte nakonfigurovat zdroje dat a porovnat jejich hodnoty s hodnotami polí **Výčet** tabulky aplikací. Výsledek porovnání musíte použít k vyplnění příslušných polí datového modelu.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Výčet**.
2. Přidejte nový zdroj dat, který bude použit pro přístup k hodnotám výčtu **EnumAppNoYes**:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V dialogovém okně do pole **Název** zadejte **EnumAppNoYes**.
    3. Do pole **Výčet** zadejte **NoYes**.
    4. Vyberte **OK** pro přidání nového zdroje dat.

3. V podokně **Typy zdrojů dat** vyberte **Dynamics 365 for Operations\\Výčet**.
4. Přidejte nový zdroj dat, který bude použit pro přístup k hodnotám výčtu **KMCollectionQuestionMode**:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V rozevíracím dialogovém okně do pole **Název** zadejte **EnumAppQuestionOrder**.
    3. Do pole **Výčet** zadejte **KMCollectionQuestionMode**.
    4. Vyberte **OK** pro přidání nového zdroje dat.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Přidání štítků ER a vygenerování sestavy ve specifikovaném jazyce

Můžete přidat popisky ER a nakonfigurovat některé zdroje dat tak, aby vrátily hodnoty, které závisí na jazyce, který je definován v kontextu volání mapování modelu.

1. Na stránce **Návrhář mapování modelu** v podokně **Datové zdroje** zvolte **Odpověď** a poté zvolte **Upravit**.
2. Aktivujte pole **Popisek**.
3. Vyberte **Přeložit**.
4. V dialogovém okně **Překlad textu** proveďte následující kroky:

    1. Do pole **ID popisku** zadejte **PositiveAnswer**.
    2. Do pole **Text ve výchozím jazyce** zadejte **Ano**.
    3. Vyberte **Přeložit**.
    4. Do pole **ID popisku** zadejte **NegativeAnswer**.
    5. Do pole **Text ve výchozím jazyce** zadejte **Ne**.
    6. Vyberte **Přeložit**.

5. Zavřete **Překlad textu** dialogové okno.
6. Vyberte možnost **Zrušit**.

![Přidejte označení ER pro mapování upravitelného modelu.](./media/er-quick-start1-adding-labels.png)

Zadali jste označení ER pouze pro výchozí jazyk. Informace o tom, jak lze štítky ER překládat do jiných jazyků, naleznete v části [Navrhujte vícejazyčné zprávy](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Přidání zdroje dat pro transformaci výsledků porovnání hodnot výčtu k textové hodnotě

Protože je nutné transformovat výsledky porovnání mezi hodnotami výčtu a textovými hodnotami několikrát pro různé zdroje, je vhodné tuto logiku nakonfigurovat jako jediný zdroj dat. Chcete-li však tento zdroj dat znovu použít, musíte jej nakonfigurovat jako parametrizovaný zdroj dat. Další informace naleznete v [Podpora parametrizovaných volání datových zdrojů elektronického výkaznictví typu vypočítaného pole](er-calculated-field-type.md)

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Obecné\\Prázdný kontejner**.
2. Přidání nového zdroje dat typu kontejner:

    1. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    2. V dialogovém okně do pole **Název** zadejte **Pomocník**.
    3. Vyberte **OK** pro přidání nového zdroje dat typu kontejner.

3. V podokně **Typy zdrojů dat** vyberte **Funkce\\Vypočítané pole**.
4. Přidání nového zdroje dat:

    1. V podokně **Zdroje dat** vyberte **Pomocník**.
    2. Vyberte **přidat**.
    3. V dialogovém okně do pole **Název** zadejte **NoYesEnumToString**.
    4. Vyberte možnost **Upravit vzorec**.
    5. V editoru vzorců vyberte **Parametry**.
    6. Chcete-li určit měrnou jednotku pro konfigurovaný výraz, postupujte takto

        1. Zvolte **Nové**.
        2. V dialogovém okně do pole **Název** zadejte **Argument**.
        3. V poli **Typ** vyberte datový typ **Logický**.
        4. Vyberte **OK**.

    7. Do pole **Vzorec** zadejte **IF (Argument = true, \@"GER\_LABEL: PositiveAnswer", \@"GER\_LABEL: NegativeAnswer ")** pro vrácení textu příslušného označení ER, v závislosti na jazyce prováděcího kontextu a hodnotě zadaného parametru.
    8. Zvolte **Uložit** a pak zavřete editor vzorců.
    9. Vyberte **OK** pro přidání nového zdroje dat.

![Konfigurovaný model mapování v návrháři mapového modelu ER.](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Navázání zdroje dat na pole zdrojů dat

Konfigurované zdroje dat musíte svázat s poli datového modelu a určit, jak bude datový model vyplněn aplikačními daty za běhu.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **CompanyName**.
2. V podokně **Zdroje dat** rozbalte **CompanyInfo** a poté postupujte takto:

    1. Rozbalte **CompanyInfo.find()** uzel, který představuje **find()** metodu tabulky CompanyInfo.
    2. Vyberte **CompanyInfo.find().Name**.
    3. Vyberte **Navázat** k vyplnění názvu společnosti, který nakonfigurovaný model mapování volá v kontextu za běhu.

3. V podokně **Datový model** vyberte **Dotazník**.
4. V podokně **Zdroje dat** vyberte **Dotazník** a poté vyberte **Navázat** k vyplnění záznamu dotazníku.
5. V podokně **Datový model** rozbalte **Questionnaire** a poté postupujte takto:

    1. V podokně **Datový model** vyberte **Aktivní**.
    2. V podokně **Datový model** vyberte **Upravit**.
    3. Do pole **Vzorec** zadejte **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** k vyplnění textově závislého a jazykově závislého výsledku porovnání mezi hodnotami výčtu.

6. Stejným způsobem pokračujte ve vázání zdrojů dat na pole datového modelu, dokud nedosáhnete následujícího výsledku.

    | Cesta pole                                              | Datový typ   | Akce | Výraz vazby |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Řetězec      | Vazba   | CompanyInfo.'find()'.Name |
    | Dotazník                                           | Seznam záznamů | Vazba   | Dotazník |
    | Questionnaire\\Active                                   | Řetězec      | Úpravy   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | Řetězec      | Vazba   | \@.kmCollectionId |
    | Questionnaire\\Description                              | Řetězec      | Vazba   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | Řetězec      | Vazba   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | Řetězec      | Úpravy   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (procento v dotazníku)",<br>EnumAppQuestionOrder.RandomGroup, "Random (procento ve skupině výsledků)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | Záznam      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | Řetězec      | Vazba   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | Řetězec      | Vazba   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Reálný        | Vazba   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Seznam záznamů | Vazba   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Celé číslo     | Vazba   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | Řetězec      | Vazba   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | Řetězec      | Úpravy   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | Řetězec      | Vazba   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Celé číslo     | Vazba   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | Řetězec      | Vazba   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Seznam záznamů | Vazba   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | Řetězec      | Úpravy   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Reálný        | Vazba   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Celé číslo     | Vazba   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | Řetězec      | Vazba   | \@.text |

    Následující obrázek ukazuje konečný stav konfigurovaných mapování modelu na stránce **Návrhář mapování modelu**.

    ![Plně konfigurovaný model mapování v návrháři mapového modelu ER.](./media/er-quick-start1-mapping2.png)

7. Uložte změny.
8. Zavřete stránku **Návrhář mapování modelu**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Dokončení návrhu mapování modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Mapování dotazníku**.
3. Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
4. Vyberte **Změnit stav** \> **Dokončeno**.

Stav verze 1.1 této konfigurace se změní z **Návrh** na **Dokončeno**. Verzi 1.1 již nelze změnit. Tato verze obsahuje konfigurovaný model mapování a lze ji použít jako základ pro další konfigurace ER. Verze 1.2 této konfigurace je vytvořena a má stav **Návrh**. Tuto verzi můžete upravit a tak upravit konfiguraci **Mapování dotazníku**.

![Verze konfigurovatelné konfigurace ER na stránce Konfigurace.](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Konfigurované mapování modelu je vaše implementace abstraktního datového modelu specifického pro Finance, který představuje obchodní doménu **Dotazník**.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Navrhněte šablonu pro vlastní sestavu

Architektura elektronického výkaznictví používá předdefinované šablony ve formátech Microsoft Office (sešity aplikace Excel nebo dokumenty aplikace Word). Při generování požadované sestavy je šablona podle požadovaných datových toků vyplněna požadovanými daty. Proto musíte nejprve vytvořit šablonu pro vlastní sestavu. Tato šablona musí být navržena jako sešit aplikace Excel, jehož struktura představuje rozložení vlastní sestavy. Musíte pojmenovat každou položku aplikace Excel, kterou chcete vyplnit požadovanými údaji.

1. Stáhněte si soubor [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) a uložte jej do místního počítače.
2. Otevřete soubor v aplikaci Excel a zkontrolujte strukturu sešitu.

Jak ukazuje následující obrázek, stažená šablona byla navržena pro tisk specifických dotazníků, které představují otázky v dotazníku, spolu s příslušnými odpověďmi.

![Šablona Excel pro tisk zadaných dotazníků.](./media/er-quick-start1-template-layout.png)

Do této šablony byly přidány názvy z Excelu, aby se vyplnily podrobnosti dotazníku. Pomocí Správce jmen můžete zkontrolovat názvy z Excelu.

![Pomocí Správce jmen můžete zkontrolovat názvy z Excelu v dodané šabloně Excel.](./media/er-quick-start1-template-names.png)

Štítky přehledů byly přidány jako pevný text v anglickém jazyce. Štítky výkazů můžete nahradit novými názvy z aplikace Excel, které vyplní štítky textem závislým na jazyce pomocí [štítků](#AddMmLabels) formátu ER, jako jste to udělali pro výrazy závislé na jazyce v konfigurovaném mapování modelu. V tomto případě musí být štítky ER přidány v upravitelném formátu ER.

Jak ukazuje následující obrázek, byla určena záhlaví vlastní sestavy, aby aplikace Excel mohla stránkovat.

![Vlastní záhlaví sestavy v poskytnuté šabloně Excel.](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Návrh formátu

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte vytvořit novou konfiguraci ER, která obsahuje komponent [formát](general-electronic-reporting.md#FormatComponentOutbound). Komponent formátu musíte nakonfigurovat, abyste určili, jak bude šablona výkazu vyplněna požadovanými daty za běhu.

Dokončením kroků v části [Import navrženého formátu konfigurace](#FormatImport) můžete importovat požadovaný formát z poskytnutého souboru XML. Alternativně můžete dokončit kroky v sekci [Vytvoření nové konfigurace formátu](#FormatCreate), chcete-li navrhnout tento formát od začátku.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Import navrženého formátu konfigurace

1. Stáhněte si soubor [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Questionnaires format.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

Chcete-li pokračovat, přeskočte další postup, [Vytvoření nové konfigurace formátu](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Vytvoření nové konfigurace formátu
 
1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Model dotazníku**.
3. Vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně proveďte následující kroky:

    1. V poli **Nový** vyberte **Formát založený na datovém modelu pro dotazníky**'.
    2. Do pole **Název** zadejte **Setava dotazníku**'.
    3. V poli **Verze datového modelu** vyberte **1**.

        > [!NOTE]
        > - Pokud vyberete konkrétní verzi základního datového modelu, zobrazí se vám struktura odpovídající verze datového modelu jako struktura zdroje dat **Modelu** ve formátu, který je vytvořen.
        > - Toto pole můžete ponechat prázdné. V takovém případě struktura verze **Návrh** datového modelu vám bude zobrazena jako struktura zdroje dat **Modelu** ve formátu, který je vytvořen. Poté můžete svůj model upravit a změny okamžitě zobrazit ve svém formátu. Tento přístup může zlepšit účinnost návrhu řešení ER když konfigurujete svůj datový model, mapování modelu a formátování současně.
        > - Pokud vyberete konkrétní verzi základního datového modelu, můžete přepnout na **Návrh** verzi později, když začnete upravovat formát.

    4. V poli **Definice datového modelu** vyberte definici **Kořen**.

5. Vytvořte konfiguraci zvolením **Vytvořit konfiguraci**.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Import šablony sestavy

1. Na stránce **Konfigurace** vyberte v konfiguračním stromu **Sestava dotazníku**.
2. Vyberte **Návrhář** pro zahájení konfigurace vlastního formátu.
3. Na stránce **Návrhář formátu** v podokně akcí vyberte **Importovat** \> **Importovat z Excelu**.
4. V dialogovém okně proveďte následující kroky:

    1. Vyberte **Přidat šablonu**.
    2. Vyhledejte a vyberte místně uložený soubor **Questionnaires report template.xslx** a vyberte **Otevřít**.
    3. Kliknutím na tlačítko **OK** importujte šablonu.

    ![Import šablony sestavy.](./media/er-quick-start1-template-import.png)

**Excel\\Soubor** prvek formátu je automaticky přidán do upravitelného formátu jako kořenový element. Navíc buď **Excel\\Rozsah** prvek formátu nebo **Excel\\Buňka** element formátu je automaticky přidán pro každý rozpoznaný Excelový název importované šablony. **Excel\\Záhlaví** formát, který má vnořený **Řetězcový** prvek je automaticky přidán, aby odrážel nastavení záhlaví importované šablony.

![Struktura formátu, která zahrnuje automaticky přidané prvky v návrháři operace ER.](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Konfigurace formátu

1. Na stránce **Návrhář formátů**, ve stromové struktuře, vyberte **Excel** kořenový prvek.
2. V kartě **Formát** na pravé straně stránky v poli **Název** zadejte <a name="AddFormatRootElement"></a>**Sestava**.
3. V poli **Jazykové předvolba** vyberte **Uživatelské předvolby** ke spuštění sestavy v preferovaném jazyce uživatele.
4. V poli **Předvolby jazykové verze** vyberte **Uživatelské předvolby** ke spuštění sestavy v preferované jazykové verzi uživatele.

    Informace o tom, jak určit jazykové a kulturní kontexty pro proces ER, viz [Návrh vícejazyčných sestav](er-design-multilingual-reports.md).

    ![Konfigurace nastavení jazyka a kultury pro navrženou sestavu v návrháři operace ER.](./media/er-quick-start1-template-format-structure1.png)

5. Ve stromu formátu rozbalte kořenový uzel a poté vyberte **ResultsGroup**.
6. Na kartě **Formát**, pole **Směr replikace**, vyberte **Žádná replikace**, protože neočekáváte, že pro jeden dotazník budete mít více skupin výsledků.

    ![Definování směru replikace pro prvky formátu Oblast v návrháři operací ER.](./media/er-quick-start1-template-format-structure2.png)

7. Zvolte možnost **Uložit**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Definice datové vazby pro název sestavy

Musíte zadat datovou vazbu pro prvek formátu, který se používá k vyplnění názvu generované sestavy.

1. Na stránce **Návrhář formátu** na kartě **Mapování** napravo, vyberte ve stromu formátu prvek **Sestavení\\ReportTile**.
2. Vyberte možnost **Upravit vzorec**.
3. V editoru vzorců vyberte **Přeložit**.
4. V dialogovém okně **Překlad textu** proveďte následující kroky:

    1. Do pole **ID popisku** zadejte **ReportTitle**.
    2. Do pole **Text ve výchozím jazyce** zadejte **Sestava dotazníků**.
    3. Vyberte **Přeložit** a potom **Uložit**.
    4. Vyberte **Přeložit** pro zavření dialogového okna **Překlad textu**.

5. Zavřete editor vzorců.

    ![Konfigurace vazby k vyplnění názvu generované sestavy.](./media/er-quick-start1-add-report-title-label.png)

Tuto techniku můžete použít k tomu, aby všechny ostatní štítky aktuální šablony byly závislé na jazyce. Informace o tom, jak mohou být přidané štítky jedné konfigurace ER přeloženy do všech podporovaných jazyků, viz [Návrh vícejazyčných sestav](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Kontrola zdrojových data modelu

1. Na stránce **Návrhář formátů**, na kartě **Mapování** vyberte záložku <a name="ModelDSName"></a>**model** zdrojových dat, který představuje základní datový model tohoto formátu ER.
2. Vyberte možnost **Upravit**.
3. Přečtěte si informace v dialogovém okně **Vlastnosti zdroje dat**. Tento zdroj dat představuje verzi 1 **Dotazníkového** komponentu datového modelu, který je umístěný v **Model dotazníků** ER konfigurace.

![Vlastnosti modelu zdroje dat v návrháři operací ER.](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Vázání prvků formátu na pole zdroje dat

Chcete-li určit, jak je šablona vyplněna za běhu, musíte svázat každý prvek formátu, který je spojen s příslušným názvem Excelu, s jediným polem zdroje dat tohoto formátu.

1. Na stránce **Návrhář formátů**, ve stromové struktuře, vyberte **Sestava\\CompanyName** prvek formátu.
2. Na záložce **Mapování** vyberte **model.CompanyName** pole zdroje dat typu **Řetězec**.
3. Vyberte **Svázat** k zadání názvu společnosti do šablony.
4. Ve stromu formátů vyberte prvek **Sestava\\Dotazník**.
5. Na záložce **Mapování** vyberte **model.Questionnaire** pole zdroje dat typu **Seznam záznamů**.
6. Vyberte možnost **vazba**.
7. Výběrem **Ukázat podrobnosti** zobrazíte další podrobnosti o prvcích formátu.

    Prvek formátu rozsahu **Dotazník** je nakonfigurován jako vertikálně replikovaný. Když je vázán na zdroj dat typu **Seznam záznamů**, vhodný **Dotazník** rozsahu šablony Excel se opakuje pro každý záznam vázaného zdroje dat.
 
    ![Vazba prvku formátu dotazníku na příslušný zdroj dat seznamu záznamů v návrháři operací ER.](./media/er-quick-start1-bindings1.png)

    Protože rozsah **Dotazník** šablony Excel je definován mezi řádky 5 až 14, tyto řádky se opakují pro každý vykazovaný dotazník.

    ![Řádky v šabloně Excel, které se budou opakovat ve vygenerované sestavě pro každý záznam ze zdrojů dat seznamu záznamů.](./media/er-quick-start1-template-questionnaire-range.png)

8. Nakonfigurujte podobné vazby pro zbývající prvky formátu, jak je popsáno v následující tabulce.

    > [!NOTE]
    > V této tabulce se předpokládá, že informace obsažené ve sloupci "Cesta ke zdroji dat" jsou pravdivé pouze při zapnuté funkci [relativní cesta](relative-path-data-bindings-er-models-format.md) ER.

    | Formát cesty prvku                                      | Cesta ke zdroji dat |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, kde **\@** je **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, kde **\@** je **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, kde **\@** je **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Po dokončení zvolte **Uložit**.

Následující obrázek ukazuje konečný stav mapování konfigurovaných datových vazeb na stránce **Návrhář formátu**.

![Konfigurované datové vazby v návrháři operace ER.](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Celá sbírka specifikovaných zdrojů dat a vazeb představuje komponentu mapování formátu konfigurovaného formátu. Toto mapování formátu je zavoláno při spuštění konfigurovaného formátu pro generování sestav.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Spuštění navrženého formátu z ER

Nyní můžete spustit navržený formát pro účely testování ze stránky **Konfigurace**.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.
3. Vyberte **Návrhář** pro verzi formátu, která má stav **Návrh**.
4. Na stránce **Návrhář formátu** zvolte **Spustit**.
5. V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
6. Možnost filtrování potvrďte výběrem tlačítka **OK**.
7. Klepnutím na tlačítko **OK** sestavu spustíte.
8. Prohlédněte si generovanou sestavu.

Ve [výchozím nastavení](electronic-reporting-destinations.md#default-behavior) se vygenerovaná zpráva doručí jako soubor Excelu, který si můžete stáhnout. Následující obrázky ukazují dvě stránky generované zprávy ve formátu Excel.

![Příklad vygenerované sestavy ve formátu Excel, strana 1.](./media/er-quick-start1-report1a.png)

![Příklad vygenerované sestavy ve formátu Excel, strana 2.](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Vylaďte navržený formát

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Upravte formát a změňte název generovaného dokumentu

Ve výchozím nastavení je vygenerovaný dokument pojmenován pomocí aliasu aktuálního uživatele. Úpravou formátu můžete toto chování změnit tak, aby byl vygenerovaný dokument pojmenován na základě vlastní logiky. Název vygenerovaného dokumentu může být například založen na aktuálním datu a času relace nebo na názvu sestavy.

1. Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.
2. Na kartě **Mapování** vyberte **Upravit název souboru**.
3. Do pole **Vzorec** zadejte **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Zvolte **Uložit** a pak zavřete editor vzorců.
5. Zvolte **Uložit**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Upravte formát a změňte pořadí otázek

Ve vygenerované sestavě nejsou otázky správně uspořádány. Pořadí můžete změnit úpravou formátu.

1. Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.
2. Na kartě **Mapování** ve stromu formátu rozbalte **Sestava\\Dotazník\\Otázka**.

    ![Prvek formátu otázek typu typu oblast v návrhář operací ER.](./media/er-quick-start1-bindings3.png)

3. Na kartě **Mapování** vyberte **model.Questionnaire**.
4. Vyberte **Přidat** \> **Funkce\\Vypočítané pole** a pak v poli **Název** zadejte **OrderedQuestions**.
5. Vyberte možnost **Upravit vzorec**.
6. V editoru vzorců do pole **Vzorec** zadejte **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** pro uspořádání seznamu otázek aktuálního dotazníku podle pořadového čísla.
7. Zvolte **Uložit** a pak zavřete editor vzorců.
8. Vyberte **OK** pro dokončení zadání nového vypočítaného pole.
9. Na kartě **Mapování** vyberte **model.Questionnaire.OrderedQuestions**.
10. Ve stromu formátu vyberte **Excel\\Dotazník\\Otázka**.
11. Vyberte **Svázat** a poté potvrďte, že aktuální **model.Questionnaire.Questions** cesta je nahrazena novou **model.Questionnaire.OrderedQuestions** cestou ve všech vazbách vnořených prvků.
12. Zvolte **Uložit**.

![Vazba prvku formátu Otázka na konfigurovaný zdroj dat OrderedQuestions v Návrháři operací ER.](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Spuštění upraveného formátu z ER

Nyní můžete spouštět upravený formát pro účely testování z rozhraní ER.

1. Na stránce **Návrhář formátu** zvolte **Spustit**.
2. V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
3. Možnost filtrování potvrďte výběrem tlačítka **OK**.
4. Klepnutím na tlačítko **OK** sestavu spustíte.
5. Prohlédněte si generovanou sestavu.

Následující obrázek ukazuje vygenerovanou sestavu ve formátu Excel, kde jsou otázky správně uspořádány.

![Generovaná sestava ve formátu Excel, která má správně uspořádané otázky.](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Dokončete návrh formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.
3. Na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
4. Vyberte **Změnit stav** \> **Dokončeno**.

Stav verze 1.1 této konfigurace se změní z **Návrh** na **Dokončeno**. Verzi 1.1 již nelze změnit. Tato verze obsahuje nakonfigurovaný formát a lze ji použít k vytištění vlastní sestavy. Verze 1.2 této konfigurace je vytvořena a má stav **Návrh**. Tuto verzi můžete upravit a tak upravit formát vašeho sestavení **Dotazníku**.

![Upravitelné konfigurace ER na stránce Konfigurace.](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Konfigurovaný formát je váš návrh sestavení **Dotazníku** a neobsahuje žádné vztahy k artefaktům specifickým pro Finance.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Vytvořte artefakty aplikace a pojmenujte navrženou sestavu

Jako uživatel v roli správce systému musíte vyvinout novou logiku, aby nakonfigurovaný formát ER mohl být vyvolán z uživatelského rozhraní aplikace (UI) pro vygenerování vaší vlastní sestavy. V současné době ER nenabízí žádné možnosti pro konfiguraci tohoto typu logiky. Proto je nutné provést určité inženýrské práce. 

Pro vyvinutí nové logiky je nutné nasadit topologii, která podporuje průběžné sestavování. Další informace naleznete v tématu [Nasazení topologií, které podporují automatizaci průběžného sestavení a testů](../perf-test/continuous-build-test-automation.md). Také musí mít přístup k vývojovému prostředí pro tuto topologii. Další informace o dostupných ER API najdete v tématu [API rozhraní architektury elektronického výkaznictví](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Úprava zdrojového kódu

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Přidejte třídu datového kontraktu

Přidejte nový **DotazníkyErReportContract** třídu do Microsoft Visual Studio projektu a napište kód, který specifikuje datový kontrakt, který by měl být použit pro spuštění nakonfigurovaného formátu ER.

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

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Přidejte třídu tvůrce uživatelského rozhraní

Přidejte novou **DotazníkyReportUIBuilder** třídu do Visual Studio projektu a napiště kód pro vygenerování dialogového okna runtime, které bude použito k vyhledání ID mapování formátu formátu ER, který musí být spuštěn. Poskytovaný kód vyhledá pouze formáty ER, které obsahují zdroj dat typu **Datový model**, který odkazuje na datový model **[Dotazníky](#DataModeName)** pomocí **[Kořenové](#RootDefinitionName)** definice.

> [!NOTE]
> Alternativně můžete použít body integrace ER k filtrování formátů ER. Další informace viz [API pro zobrazení vyhledávání mapování formátu](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

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

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Přidejte třídu poskyovatele dat

Přidejte nový **QuestionnairesErReportDP** třídu do Visual Studio projektu a napište kód, který uvádí poskytovatele dat, který by měl být použit pro spuštění nakonfigurovaného formátu ER. Poskytnutý kód zahrnuje pouze datový kontrakt pro tohoto poskytovatele dat.

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

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Přidejte soubor štítků

Přidejte nový **QuestionnairesErReportLabels\_en-US** soubor štítků do vašeho Visual Studio projektu a určete následující štítky pro nové prostředky uživatelského rozhraní:

- **\@QuestionnairesReport** štítek pro novou položku nabídky, která obsahuje následující text v americké angličtině (en-US): **Sestava dotazníků (využívá ER)**
- **\@QuestionnairesReportBatchJobDescription** štítek pro název dávkové úlohy, pokud bure vybraný formát ER spuštěn jako dávková úloha

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Přidejte třídu služby sestav

Přidejte novou **QuestionnairesErReportService** třídu do vašeho Visual Studio projektu a napište kód, který volá formát ER, identifikuje jej pomocí ID mapování formátu a jako parametr poskytuje datový kontrakt.

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

Když musíte použít formát ER, který spouští aplikační data, musíte nakonfigurovat zdroj dat typu **Datový model** v mapování formátu. Tento zdroj dat odkazuje na konkrétní část specifikovaného datového modelu pomocí jediné kořenové definice. Při spuštění formátu ER tento zdroj dat žádá o přístup k příslušnému mapování modelu ER, které je nakonfigurováno pro daný model a definici kořenů.

Všechny informace, které byste mohli připravit ve zdrojovém kódu a uložit jako součást datového kontraktu, lze předat do běžícího formátu ER pomocí mapování modelu ER tohoto typu. V mapování modelu ER musíte nakonfigurovat zdroj dat typu **Objekt**, který odkazuje na třídu **[QuestionnairesErReportContract](#DataContractClass)**. Chcete-li identifikovat mapování modelu, musíte určit zdroj dat, který toto mapování modelu volá. V zadaném kódu je tento zdroj dat specifikován konstantou **ERModelDataSourceName**, která má hodnotu **[model](#ModelDSName)**. Chcete-li identifikovat, který zdroj dat se používá k vystavení datového kontraktu v mapování modelu, musíte zadat název zdroje dat. V zadaném kódu je tento název specifikován konstantou **ParametersDataSourceName**, která má hodnotu <a name="DataContractDSName"></a>**RunTimeParameters**.

> [!NOTE]
> V novém prostředí budete možná muset aktualizovat metadata ER, aby byl tento typ třídy k dispozici v návrháři mapování modelů ER. Další informace získáte v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Přidejte třídu kontrolera sestav

Přidejte novou třídu **QuestionnairesErReportController** do vašeho Visual Studio projektu a napiště kód, který spouští formát ER v synchronním režimu nebo dávkovém režimu v dialogovém okně, které je vytvořeno na základě logiky poskytované třídou **QuestionnairesErReportUIBuilder**.

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

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Přidejte položku nabídky

Přidejte novou **QuestionnairesErReport** položku nabídky do Visual Studio projektu. Ve vlastnosti **Objekt** tato položka nabídky odkazuje na třídu **QuestionnairesErReportController** a používá se k určení uživatelského oprávnění k výběru a spuštění formátu ER. Ve vlastnosti **Označení** tato položka nabídky odkazuje na štítek **\@QuestionnairesReport**, který jste vytvořili dříve, aby v uživatelském rozhraní aplikace byl uveden správný text.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Přidejte položku nabídky k nabídce

Přidejte existující **KM** menu do vašeho Visual Studio projektu. Musíte přidat novou položku **QuestionnairesErReport** typu **Výstup** do této nabídky. Tato položka musí odkazovat na **QuestionnairesErReport** položku nabídky, která je popsána v předchozí části.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Sestavte Visual Studio projekt

Vytvořte svůj projekt a zpřístupněte uživatelům novou položku nabídky.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Spusťte formát z aplikace

1. Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.

    ![Výběrem položky nabídky Přehled dotazníků (využívá ER) v modulu Dotazník spustíte nakonfigurovaní ER formát.](./media/er-quick-start1-application-menu-modified.png)

2. V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.
3. Vyberte **OK**.
4. V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
5. Možnost filtrování potvrďte výběrem tlačítka **OK**.
6. Klepnutím na tlačítko **OK** sestavu spustíte.

    ![Zadání kritérií výběru v dialogovém okně Elektronický výkaz.](./media/er-quick-start1-report-run-dialog-page.png)

7. Prohlédněte si generovanou sestavu.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Vylaďte navržené řešení ER

Konfigurované řešení ER můžete upravit tak, že používá třídu poskytovatele dat, kterou jste vyvinuli, pro přístup k podrobnostem o běžícím formátu ER a tak, že do vygenerovaného výkazu zadá název tohoto formátu ER.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Úprava mapování modelu

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Přidání zdroje dat pro přístup k objektu kontraktu dat

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Mapování dotazníku**.
3. Vyberte **Návrhář** k otevření stránky **Mapování modelu k datovým zdrojům**.
4. Vyberte **Návrhář** k otevření vybraného mapování v návrháři mapových modelů.
5. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Objekt**.
6. V podokně **Zdroje dat** vyberte **Přidat kořen**.
7. V dialogovém okně, v poli **Název**, zadejte **[RunTimeParameters](#DataContractDSName)**, jak je definováno ve zdrojovém kódu třídy **QuestionnairesErReportService**.
8. Do pole **Třída** zadejte **[QuestionnairesErReportContract](#DataContractClass)**, naprogramovaný dříve.
9. Vyberte **OK**.
10. Rozšiřte **RunTimeParameters**.

Přidaný zdroj dat poskytuje informace o ID záznamu běžícího mapování formátu ER.

![Přidán zdroj dat v návrháři mapování modelů ER.](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Přidejte zdroj dat pro přístup k záznamům mapování formátu ER

Pokračujte v úpravách mapování vybraného modelu přidáním zdroje dat pro přístup k záznamům mapování formátu ER.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Záznamy tabulky**.
2. V podokně **Zdroje dat** vyberte **Přidat kořen**.
3. V dialogovém okně do pole **Název** zadejte **ER1**.
4. Do pole **Tabulka** zadejte **ERFormatMappingTable**.
5. Vyberte **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Přidejte zdroj dat pro přístup k záznam mapování běžícího formátu ER

Pokračujte v úpravách mapování vybraného modelu přidáním zdroje dat pro přístup k záznamům mapování formátu běžícího ER formátu.

1. Na stránce **Návrhář mapování modelu** v podokně **Typy datových zdrojů** zvolte položku **Funkce\\Vypočítané pole**.
2. V podokně **Zdroje dat** vyberte **Přidat kořen**.
3. V dialogovém okně do pole **Název** zadejte **ER2**.
4. Vyberte možnost **Upravit vzorec**.
5. V editoru vzorců do pole **Vzorec** zadejte **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Zvolte **Uložit** a pak zavřete editor vzorců.
7. Vyberte **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Zadejte název datového modelu běžícího formátu ER

Pokračujte v úpravách mapování vybraného modelu tak, aby se do datového modelu zadal název běžícího formátu ER.

1. Na stránce **Návrhář mapování modelu** v podokně **Datový model** otevřete **ExecutionContext** a poté zvolte **ExecutionContext\\FormatName**.
2. V podokně **Datový model** vyberte **Upravit** pro konfiguraci vazby dat pro pole vybraného datového modelu.
3. V editoru vzorců do pole **Vzorec** zadejte **FIRSTORNULL (ER2.'\>Relations.Format).Name**.
4. Zvolte **Uložit** a pak zavřete editor vzorců.

Protože jste použili **FormatName**, v konfigurovaném mapování modelu se nyní zobrazí název formátu ER, který během provádění volá toto mapování modelu.

![Vazba pole datového modelu na metodu přidaného zdroje dat v návrháři mapování modelu ER.](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Dokončení návrhu mapování modelu

1. Na stránce **Návrhář mapování modelu** zvolte **Uložit**.
2. Zavřete stránku.
3. Zavřete stránku Mapování modelu.
4. Na stránce **Konfigurace** ve stromu konfigurace zkontrolujte, zda je konfigurace **Mapování dotazníku** stále vybrána. Poté na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
5. Vyberte **Změnit stav** \> **Dokončeno**.

Stav verze 1.2 této konfigurace se změní z **Návrh** na **Dokončeno**. Verzi 1.2 již nelze změnit. Tato verze obsahuje konfigurovaný model mapování a lze ji použít jako základ pro další konfigurace ER. Verze 1.3 této konfigurace je vytvořena a má stav **Návrh**. Tuto verzi můžete upravit a tak upravit mapování modelu **Dotazník**.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Změna formátu

Konfigurovaný formát ER můžete upravit tak, aby jeho název byl zobrazen v zápatí sestavy, která je generována při spuštění formátu ER.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Přidat nový prvek formátu.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.
3. Vyberte možnost **Návrhář**.
4. Na stránce **Návrhář formátu** vyberte kořenovou položku **Sestava**.
5. Vyberte **Přidat** pro přidání nového prveku vnořeného formátu pro vybranou kořenovou položku **Zpráva**.
6. Vyberte **Excel\\Zápatí**.
7. Do pole **Název** zadejte **Zápatí**.
8. Vyberte **Sestava\Zápatí** a pak vyberte **Přidat**.
9. Vyberte **Text\\Řetězec**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Vázání přidaného prvku formátu

1. Na stránce **Návrhář formátu**, na kartě **Mapování**, pro aktivní prvek **Zápatí\\Řetězec**, vyberte **Upravit vzorec**.
2. V editoru vzorců do pole **Vzorec** zadejte **CONCATENATE("\&C\&10 ", FORMAT(" Vygenerováno "\%1 'ER řešením', model.ExecutionContext.FormatName))**.
3. Zvolte **Uložit** a pak zavřete editor vzorců.
4. Zvolte **Uložit**.

Konfigurovaný formát byl nyní upraven tak, aby jeho nýzev byl vložený do zápatí vygenerované sestavy pomocí prvku **Zápatí\\Řetězec**.

![Přidání prvku formátu zápatí do konfigurovaného formátu v návrháři operací ER.](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Dokončete návrh formátu

1. Zavřete stránku **Návrhář formátu**.
2. Na stránce **Konfigurace** ve stromu konfigurace zkontrolujte, zda je konfigurace **Sestava dotazníku** stále vybrána. Poté na pevné záložce **Verze** vyberte verzi konfigurace se stavem **Koncept**.
3. Vyberte **Změnit stav** \> **Dokončeno**.

Stav verze 1.2 této konfigurace se změní z **Návrh** na **Dokončeno**. Verzi 1.2 již nelze změnit. Tato verze obsahuje konfigurovaný formát a lze ji použít jako základ pro další konfigurace ER. Verze 1.3 této konfigurace je vytvořena a má stav **Návrh**. Tuto verzi můžete upravit a tak upravit sestavení **Dotazník**.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Spusťte formát z aplikace

1. Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.
2. V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.
3. Vyberte **OK**.
4. V dialogovém okně **Parametry ER** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
5. Možnost filtrování potvrďte výběrem tlačítka **OK**.
6. Klepnutím na tlačítko **OK** sestavu spustíte.
7. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

Všimněte si, že zápatí generované sestavy obsahuje název formátu ER, který byl použit k jeho vygenerování.

![Vygenerovaný soubor ve formátu Excel.](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Spusťte formát z ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací položku **Model dotazníku** a poté vyberte možnost **Sestava dotazníku**.
3. V podokně akcí zvolte **Spustit**.
4. V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
5. Možnost filtrování potvrďte výběrem tlačítka **OK**.
6. Klepnutím na tlačítko **OK** sestavu spustíte.
7. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

Všimněte si, že zápatí generované sestavy neobsahuje název formátu ER, který byl použit k jeho vygenerování, protože objekt datového kontraktu nebyl předán do běžícího mapování modelu, když byl volán formátem ER, který byl spuštěn z ER.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Konfigurace cílového formátu pro náhled na obrazovce

1. Přejděte do nabídky **Správa organizace** \> **Elektronická sestava** \> **Místo určení elektronického výkaznictví**.
2. Na stránce **Cíl elektronického výkaznictví** přidejte cílový záznam pro nakonfigurovaný Formát ER **Sestava dotazníku**.
3. Na pevné záložce **Cílové místo souboru**, nastavte **Obrazovka** [cíl](er-destination-type-screen.md) pro **Sestavení** formátovací komponent, který byl [přidán](#AddFormatRootElement) jako kořenový prvek nakonfigurovaného formátu ER **Sestavení dotazníku**.
4. Na pevné záložce **Nastavení převodu PDF**, nakonfigurujte cíl pro převod zprávy do [formátu PDF](electronic-reporting-destinations.md#OutputConversionToPDF) který používá orientaci stránky **na šířku**.

![Konfigurace vlastního cíle obrazovky pro formát ER na stránce Cíle elektronického hlášení.](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Spusťte formát z aplikace a zobrazte jej jako dokument PDF

1. Jděte do **Dotazník** \> **Design** \> **Sestava dotazníků (využívá ER)**.
2. V dialogovém okně, v poli **Mapování formátu**, **Sestava dotazníků**.
3. Vyberte **OK**.
4. V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Záznamy, k zahrnutí** nakonfigurujte možnost filtrování tak, aby byl zahrnutý pouze dotazník **SBCCrsExam**.
5. Možnost filtrování potvrďte výběrem tlačítka **OK**.

    Na pevné záložce **Cíle** si všimněte, že pole **Výstup** je nastaveno na **Obrazovka**. Pokud chcete změnit nakonfigurovaný cíl, vyberte **Změna**.

    ![Dialogové okno hlášení ER runtime, kde můžete změnit nakonfigurovaný cíl.](./media/er-quick-start1-run-settings.png)

6. Klepnutím na tlačítko **OK** sestavu spustíte.
7. Zkontrolujte vygenerovaný soubor ve formátu Excel.

    ![Náhled vygenerovaného souboru ve fromátu Excel.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
- [Návrh vícejazyčných sestav](er-design-multilingual-reports.md)
- [API rozhraní architektury elektronického výkaznictví](er-apis-app73.md)
- [Funkce CASE](er-functions-logical-case.md)
- [Funkce CONCATENATE](er-functions-text-concatenate.md)
- [Funkce DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [Funkce FILTER](er-functions-list-filter.md)
- [Funkce FIRSTORNULL](er-functions-list-firstornull.md)
- [Funkce FORMAT](er-functions-text-format.md)
- [Funkce IF](er-functions-logical-if.md)
- [Funkce ORDERBY](er-functions-list-orderby.md)
- [Funkce SESSIONNOW](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
