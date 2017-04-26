---
title: "Nastavení elektronické hlášení poskytovat Power BI z Dynamics 365 pro operace s daty"
description: "Toto téma vysvětluje, jak lze použít konfiguraci elektronického vykazování (ER) k uspořádání přenosu dat v aplikaci Dynamics 365 for Operations do služeb Power BI. Toto téma používá jako příklad transakcí v systému Intrastat obchodní údaje, které je nutné převést. Vizualizace map Power BI využívá těchto dat transakcí systému Intrastat, aby představila náhled analýzy aktivit importu a exportu společnosti."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Nastavení elektronické hlášení poskytovat Power BI z Dynamics 365 pro operace s daty

Toto téma vysvětluje, jak lze použít konfiguraci elektronického vykazování (ER) k uspořádání přenosu dat v aplikaci Dynamics 365 for Operations do služeb Power BI. Toto téma používá jako příklad transakcí v systému Intrastat obchodní údaje, které je nutné převést. Vizualizace map Power BI využívá těchto dat transakcí systému Intrastat, aby představila náhled analýzy aktivit importu a exportu společnosti.

<a name="overview"></a>Přehled
--------

Microsoft Power BI je sada softwarových služeb, aplikací a konektorů, které společně mění externí zdroje dat na souvislých, vizuálně dokonalých a interaktivních poznatků. Elektronického vykazování (ER) uživatelům aplikace Microsoft Dynamics 365 for Operation umožňuje snadno konfigurovat zdroje dat a upravovat převod dat z Dynamics 365 for Operations do Power BI. Data se převádějí jako soubory ve formátu listu OpenXML (soubor sešitu aplikace Microsoft Excel). Převedené soubory se ukládají na serveru Microsoft SharePoint, který byl konfigurován pro tento účel. Uložené soubory se používají v Power BI a vyrábějí sestavy, které zahrnují vizualizace (tabulky, grafů, mapy apod.) Zprávy Power BI jsou sdíleny s uživateli Power BI a jsou dostupné na panelech Power BI a na stránkách Dynamics 365 for Operations. Toto téma vysvětluje následující úkoly:

-   Konfiguraci Microsoft Dynamics 365 for Operations
-   Přípravu konfigurace formátu ER, aby získávala data z Dynamics 365 for Operations.
-   Konfiguraci prostředí ER pro přenos dat do Power BI.
-   Použití převedených dat pro vytvoření sestavy Power BI.
-   Zpřístupnění sestavy Power BI v Dynamics 365 for Operations.

## <a name="prerequisites"></a>Předpoklady
Pro dokončení příkladu v tomto tématu, musíte mít následující přístup:

-   Přístup k aplikaci Dynamics 365 for Operations pro některou z následujících rolí:
    -   Návrhář elektronického výkaznictví
    -   Funkční konzultant elektronického výkaznictví
    -   Správce systému
-   Přístup k serveru SharePoint, který je konfigurován pro použití s Dynamics 365 for Operations
-   Přístup k systému Power BI

## <a name="configure-document-management-parameters"></a>Konfigurujte parametry správy dokumentů
1.  Na stránce **Parametry správy dokumentů**, nakonfigurujte přístup k serveru SharePoint, který bude používán ve společnosti, do které jste přihlášeni (např. společnost DEMF).
2.  Zkontrolujte připojení k serveru SharePoint, abyste se ujistili, že máte udělen přístup. [![Stránku parametry správy dokumentů](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Otevřete konfigurovanou stránku SharePoint. Vytvořte novou složku, kam bude ER ukládat Excelové soubory s obchodními údaji, které vyžadují sestavy Power BI jako zdroje sad dat Power BI.
4.  V aplikaci Dynamics 365 for Operations na stránce **Typy dokumentů** vytvořte nový typ dokumentu, který se použije pro přístup ke složce služby SharePoint, kterou jste právě vytvořili. Zadejte **soubor** do pole **Skupina** a **SharePoint** do pole **Umístění** a poté zadejte adresu složky služby SharePoint. [![Typy stránky dokumentu](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurace parametrů ER
1.  V pracovním prostoru **Elektronické sestavy** klepněte na odkaz **Parametry elektronického vykazování**.
2.  V záložce **Přílohy** vyberte typ dokumentu **Soubor** pro všechna pole.
3.  V pracovním prostoru **Elektronické sestavy** zaktivujte požadovaného poskytovatele klepnutím na tlačítko **Nastavit jako aktivní**. Pro další informace si přehrajte tutorial **Vyberte poskytovatele služeb ER**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Datový model ER můžete použít jako zdroj dat
Musíte mít datový model ER jako zdroj obchodních dat, která se použijí v sestavách Power BI. Tento datový model se nahrává z úložiště konfigurací ER. Další informace naleznete v tématu [Stáhnout konfigurace elektronického vykazování ze služby Lifecycle Services](download-electronic-reporting-configuration-lcs.md) nebo si přehrajte tutorial **ER Import konfigurace ze služby Lifecycle Services**. Vyberte **Intrastat **jako datový model, který se bude nahrávat z vybraného úložiště konfigurací ER. (V tomto příkladu 1 modelu je použita verze.) Potom můžete přistupovat **Intrastat** konfigurace modelu ER na **konfigurace** stránky. [![Stránka Konfigurace](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Navrhněte ER konfiguraci formátu
Je nutné vytvořit novou konfiguraci formátu ER, který používá datový model **Intrastat** jako zdroj obchodních dat. Tato konfigurace formátu musí generovat výsledky v podobě elektronických dokumentů formátu OpenXML (soubor aplikace Excel). Pro další důležité informace si přehrajte tutorial **ER vytvoření konfigurace pro sestavy ve formátu OPENXML**. Pojmenujte nové konfigurace **Import / export aktivit**, jak je ukázáno na následujícím obrázku. Použijte soubor v aplikaci Excel [dat ER – podrobnosti importu a exportu](https://go.microsoft.com/fwlink/?linkid=845208) jako šablonu při navrhování ER formátu. (Další informace o tom, jak importovat šablonu formátu, přehrávat úloh průvodce.) [![Import / export konfigurace aktivity](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) změnit **Import / export aktivity** formát konfigurace, postupujte takto.

1.  Klikněte na možnost **Návrhář**.
2.  V záložce **Formát** pojmenujte prvek souboru pro tento formát **výstupního souboru Excel**. [![Element soubor výstupu aplikace Excel](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  V záložce **Mapování** zadejte název souboru aplikace Excel, který bude generován při každém spuštění tohoto formátu. Konfigurujte související výraz pro návrat hodnoty **Podrobnosti importu a exportu** (.xlsx přípona se přidá automaticky). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Přidejte novou položku zdroje dat pro tento formát. (Tento výčet bude vyžadován pro vazby na další data.)
    1.  Název zdroje dat **směr\_výčtu**.
    2.  Vyberte **Výčet modelů dat** jako typ zdroje dat.
    3.  Odkazujte k výčtu modelů dat **Směr**.

    [![směr\_výčtu.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Dokončete vazbu prvků datového modelu **Intrastat** a prvků navrženého formátu, jak je ukázáno v následujícím obrázku. [![Dokončení vazby](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Po spuštění bude formát ER generovat výstupní výsledky ve formátu aplikace Excel. Odešle podrobnosti transakcí Intrastat do výstupních výsledků a oddělí je od transakcí, které popisují aktivity importní nebo exportní aktivity. Klepněte na tlačítko **spuštění** testování nového formátu ER seznam transakcí systému Intrastat v **Intrastat** stránky (**daně**&gt;**prohlášení**&gt;**zahraničního obchodu**&gt;**Intrastat**). [![Intrastat stránky](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) je generován následující výstup výsledků. Soubor je nazván **Detaily importu a exportu.xlsx**, jak jste zadali v nastavení formátu. [![Import a export details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurujte cíle ER
Je nutné konfigurovat systém ER pro odeslání výstupních výsledků nové konfigurace formátu ER zvláštním způsobem.

-   Výstupní výsledek musí být zaslán do složky vybraného serveru SharePoint.
-   Každé provedení konfigurace formátu musí vytvořit novou verzi stejného souboru aplikace Excel.

Na **elektronických sestav** stránky (**Správa organizace**&gt;**elektronických sestav**), klepněte **elektronické hlášení cíl** položky a přidat nové umístění. V poli**odkazy** vyberte konfiguraci formátu **Aktivity importu / exportu aktivity**, kterou jste předtím vytvořili. Tento postup slouží k přidání nového záznamu cílového souboru pro odkaz.

1.  V poli **název** zadejte název cíle souboru.
2.  V poli **Název souboru** vyberte název **Výstupního souboru Excel** coby součást formátu souboru aplikace Excel.

Klepněte na tlačítko **Nastavení** pro nový záznam cíle. Potom můžete v dialogovém okně **nastavení cíle** provést následující kroky.

1.  V záložce **Power BI** nastavte možnost **povoleno** na **Ano**.
2.  V poli **SharePoint** vyberte typ dokumentu **Sdílené**, který jste vytvořili dříve.

## <a name="schedule-execution-of-the-configured-er-format"></a>Naplánujte provedení konfigurovaného ER formátu
Na **konfigurace** stránky (**Správa organizace**&gt;**elektronických sestav**&gt;**konfigurace**), vybrat ve stromové struktuře konfigurace **Import / export aktivity** konfigurace, kterou jste vytvořili dříve. Změňte stav verze 1.1 z **Koncept** na **dokončeno**, abyste tento formát zpřístupnili pro používání. [![Konfigurace stránky](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) vyberte dokončenou verzi **Import / export aktivity** konfigurace a potom klepněte na tlačítko **spuštění**. Všimněte si, že konfigurovaný cíl se aplikuje na výstupní výsledek vytvořený ve formátu aplikace Excel. Nastavte možnost **Dávkové zpracování** na **Ano**, čímž spustíte tuto sestavu v bezobslužném režimu. Klepněte na tlačítko **Opakování**, abyste mohli naplánovat požadované opakování spuštění této dávky. Opakování definuje, jak často se budou aktualizovaná data přesouvat z Dynamics 365 for Operations do Power BI. [![Dialogové okno Parametry elektronické sestavy](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) konfigurován, můžete najít úlohy spuštění sestavy ER na **dávkové úlohy** stránky (**Správa systému &gt;dotazy &gt;dávkové úlohy**). [![Dávkové úlohy stránky](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) při spuštění této úlohy první cíl vytvoří nový soubor aplikace Excel, který byl nakonfigurovaný název vybrané složky služby SharePoint. Při každém dalším spuštění úkolu cíl vytvoří novou verzi souboru aplikace Excel. [![Nová verze souboru aplikace Excel](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Vytvořte sadu dat Power BI s použitím výstupního výsledku ER formátu
Přihlaste se k Power BI a buď otevřete existující skupinu Power BI (pracovní prostor) nebo vytvořte novou skupinu. Klepněte buď na **přidat** pod **soubory** v **importovat nebo připojit k datům** oddílu, nebo klepněte na znaménko plus (**+**) vedle **datových sad** v levém podokně. [![Vytváření objektu dataset](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) vybrat **SharePoint – týmové weby** možnost a potom zadejte cestu serveru SharePoint, který používáte (**https://ax7partner.spoppe.com** v našem příkladu). Přejděte do složky **Sdílené dokumenty / GER data / PowerBI** a vyberte soubor aplikace Excel, který jste vytvořili jako zdroj dat pro novou sadu dat Power BI. [![Vyberte soubor aplikace Excel](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) klepněte na tlačítko **připojit**a potom klepněte na tlačítko **Import**. Vytvoří se nová sada dat na základě vybraného souboru aplikace Excel. Sadu dat lze také automaticky přidávat do nově vytvořeného řídicího panelu. [![Objekt DataSet na řídicím panelu](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) konfigurace aktualizace plánu pro tento objekt dataset Chcete-li vynutit periodické aktualizace. Pravidelné aktualizace umožňují spotřebu nových obchodních dat, které pocházejí z Dynamics 365 for Operations prostřednictvím periodického spouštění sestavy ER prostřednictvím nových verzí souboru aplikace Excel, které se vytvářejí na serveru SharePoint Server.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Vytvořte sestavu Power BI pomocí nové sady dat
Chcete-li vytvořit novou sestavu Power BI, klepněte na tlačítko **podrobnosti importu a exportu** sady dat Power BI, které jste vytvořili. Nakonfigurujte potom zobrazení. Vyberte například vizualizaci **Plná mapa** a proveďte její konfiguraci následujícím způsobem:

-   Přiřaďte sadu dat **CountryOrigin** do pole **Umístění** vizualizace mapy.
-   Přiřaďte sadu dat **Množství** do pole **Sytost barvy** vizualizace mapy.
-   Přidejte pole sad dat **aktivity** a **Rok** k polím **Filtry** kolekce vizualizace map.

Uložte sestavu Power BI jako **sestava podrobností o Importu a exportu**. [![Import a export sestavy Podrobnosti o](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Všimněte si, že zobrazí mapy zemí nebo oblastí, které jsou uvedeny v souboru aplikace Excel (Rakousko a Švýcarsko v tomto příkladu). Tyto země/oblasti se vybarví, aby zobrazily podíl fakturovaných částek pro každou z nich. Aktualizujte seznam transakcí v systému Intrastat. Byla přidána transakce exportu, která pochází z Itálie. [![Seznam transakcí systému Intrastat](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) čekat na další naplánované spuštění sestavy ER a další plánované aktualizace datové sady Power BI. Potom zkontrolujte sestavu Power BI (vyberte pro zobrazení pouze transakcí importu). Aktualizovaná mapa nyní zobrazuje Itálii. [![Aktualizované mapy](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Zpřístupnění sestavy Power BI v Dynamics 365 for Operations
Nastavte integraci mezi Dynamics 365 for Operations a Power BI. Další informace naleznete na [konfigurace integrace Power BI pro pracovní prostory](configure-power-bi-integration.md). Na **elektronických sestav** stránku pracovního prostoru, která podporuje integraci Power BI (**Správa organizace**&gt;**pracovní prostory**&gt;**elektronických sestav pracovního prostoru**), klepněte na tlačítko **možnosti**&gt;**otevřít sestavu katalogu**. Vyberte **Podrobnosti Importu a exportu** sestavy Power BI, kterou jste vytvořili, aby se tato sestava zobrazila jako položka akcí na vybrané stránce. Klepněte na položku akce, abyste otevřeli stránku 365 Dynamics for Operations, která ukazuje sestavy, které jste navrhli v Power BI. [![Import a export sestavy podrobností](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Viz také
--------

[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


