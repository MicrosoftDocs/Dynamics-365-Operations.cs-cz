---
title: Konfigurace elektronického výkaznictví pro doplňování dat do Power BI
description: Tento článek vysvětluje, jak lze použít konfiguraci elektronického vykazování (ER) k uspořádání přenosu dat z vaší instance do služeb Power BI.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6903513dec4da20dbc4463fbae6a406fc06e1a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896727"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Konfigurace elektronického výkaznictví pro doplňování dat do Power BI

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak lze použít konfiguraci elektronického vykazování (ER) k uspořádání přenosu dat z vaší instance do služeb Power BI. Tento článek používá jako příklad transakcí v systému Intrastat obchodní údaje, které je nutné převést. Vizualizace map Power BI využívá těchto dat transakcí systému Intrastat, aby představila náhled analýzy aktivit importu a exportu společnosti v sestavě Power BI.

## <a name="overview"></a>Přehled

Microsoft Power BI je sada softwarových služeb, aplikací a konektorů, které společně mění externí zdroje dat na souvislých, vizuálně dokonalých a interaktivních poznatků. Elektronické výkaznictví umožňuje uživatelům snadno konfigurovat zdroje dat a převod dat z aplikace do Power BI. Data se převádějí jako soubory ve formátu listu OpenXML (soubor sešitu aplikace Microsoft Excel). Převedené soubory se ukládají na serveru Microsoft SharePoint, který byl konfigurován pro tento účel. Uložené soubory se používají v Power BI a vyrábějí sestavy, které zahrnují vizualizace (tabulky, grafů, mapy apod.) Sestavy Power BI se sdílí s uživateli Power BI a jsou dostupné na řídicích panelech Power BI a na stránkách aplikace. Tento článek vysvětluje následující úkoly:

- Konfigurace Microsoft Dynamics 365 Finance.
- Přípravu konfigurace formátu ER na získávání dat z aplikace Finance.
- Konfiguraci prostředí ER pro přenos dat do Power BI.
- Použití převedených dat pro vytvoření sestavy Power BI.
- Zpřístupnění sestavy Power BI v aplikaci Finance.

## <a name="prerequisites"></a>Předpoklady
Pro dokončení příkladu v tomto článku, musíte mít následující přístup:

- Přístup pro některou z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k serveru SharePoint, který je konfigurován k použití s aplikací.
- Přístup k architektuře Power BI

## <a name="configure-document-management-parameters"></a>Konfigurujte parametry správy dokumentů
1. Na stránce **Parametry správy dokumentů** nakonfigurujte přístup k serveru SharePoint, který bude používán ve společnosti, do které jste přihlášeni (např. společnost DEMF).
2. Zkontrolujte připojení k serveru SharePoint, abyste se ujistili, že máte udělen přístup.

    [![Stránka s parametry správy dokumentů.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Otevřete konfigurovanou stránku SharePoint. Vytvořte novou složku, kam bude elektronické výkaznictví ukládat soubory aplikace Excel s obchodními údaji, které vyžadují sestavy Power BI jako zdroje sad dat Power BI.
4. Na stránce **Typy dokumentů** vytvořte nový typ dokumentu, který se použije pro přístup ke složce služby SharePoint, kterou jste právě vytvořili. Zadejte **Soubor** do pole **Skupina** a **SharePoint** do pole **Umístění** a poté zadejte adresu složky služby SharePoint.

    [![Stránka typu dokumentu.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurace parametrů ER
1. V pracovním prostoru **Elektronické sestavy** klepněte na odkaz **Parametry elektronického vykazování**.
2. V záložce **Přílohy** vyberte typ dokumentu **Soubor** pro všechna pole.
3. V pracovním prostoru **Elektronické sestavy** zaktivujte požadovaného poskytovatele klepnutím na tlačítko **Nastavit jako aktivní**. Pro další informace si přehrajte tutorial **Vyberte poskytovatele služeb ER**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Datový model ER můžete použít jako zdroj dat
Musíte mít datový model ER jako zdroj obchodních dat, která se použijí v sestavách Power BI. Tento datový model se nahrává z úložiště konfigurací ER. Další informace naleznete v tématu [Stáhnout konfigurace elektronického vykazování ze služby Lifecycle Services](download-electronic-reporting-configuration-lcs.md) nebo si přehrajte tutorial **ER Import konfigurace ze služby Lifecycle Services**. Vyberte **Intrastat** jako datový model, který se bude nahrávat z vybraného úložiště konfigurací ER. (V tomto příkladu je použita verze 1 modelu.) Potom můžete přistupovat ke konfiguraci modelu **Intrastat** na stránce **Konfigurace**.

[![Konfigurace modelu Intrastat ER na stránce Konfigurace.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Navrhněte ER konfiguraci formátu
Je nutné vytvořit novou konfiguraci formátu ER, který používá datový model **Intrastat** jako zdroj obchodních dat. Tato konfigurace formátu musí generovat výsledky v podobě elektronických dokumentů formátu OpenXML (soubor aplikace Excel). Pro další důležité informace si přehrajte tutorial **ER vytvoření konfigurace pro sestavy ve formátu OPENXML**. Pojmenujte nové konfigurace **Import / export aktivit**, jak je ukázáno na následujícím obrázku. Použijte soubor v aplikaci Excel [dat ER – podrobnosti importu a exportu](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx) jako šablonu při navrhování ER formátu. (Pro informace o šabloně formátu importu si přehrajte tutorial.)

[![Konfigurace aktivit import/export.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Pro změnu konfigurace formátu **Import / export aktivit** postupujte takto.

1. Klikněte na možnost **Návrhář**.
2. V záložce **Formát** pojmenujte prvek souboru pro tento formát **výstupního souboru Excel**.

    [![Prvek výstupního souboru v aplikaci Excel.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. V záložce **Mapování** zadejte název souboru aplikace Excel, který bude generován při každém spuštění tohoto formátu. Konfigurujte související výraz pro návrat hodnoty **Podrobnosti importu a exportu** (.xlsx přípona se přidá automaticky).

    [![Návrhář formátu.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Přidejte novou položku zdroje dat pro tento formát. (Tento výčet bude vyžadován pro vazby na další data.)

    1. Pojmenujte zdroj dat **direction\_enum**.
    2. Vyberte **Výčet modelů dat** jako typ zdroje dat.
    3. Odkazujte k výčtu modelů dat **Směr**.

    [![direction_enum.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Dokončete vazbu prvků datového modelu **Intrastat** a prvků navrženého formátu, jak je ukázáno v následujícím obrázku.

    [![Dokončení vazby.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Po spuštění bude formát ER generovat výstupní výsledky ve formátu aplikace Excel. Odešle podrobnosti transakcí Intrastat do výstupních výsledků a oddělí je od transakcí, které popisují aktivity importní nebo exportní aktivity. Klikněte na **Spustit** pro testování nového formátu seznamu transakcí na stránce **Intrastat** (**Daň** &gt; **Prohlášení** &gt; **Zahraniční obchod** &gt; **Intrastat**).

[![Stránka Intrastat.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Vygeneruje se následující výstupní výsledek. Soubor je nazván **Detaily importu a exportu.xlsx**, jak jste zadali v nastavení formátu.

[![Detaily importu a exportu.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurujte cíle ER
Je nutné konfigurovat systém ER pro odeslání výstupních výsledků nové konfigurace formátu ER zvláštním způsobem.

- Výstupní výsledek musí být zaslán do složky vybraného serveru SharePoint.
- Každé provedení konfigurace formátu musí vytvořit novou verzi stejného souboru aplikace Excel.

Na stránce **Elektronické sestavy** (**Správa organizace** &gt; **Elektronické vykazování**) klikněte na **Cíl elektronického vykazování** a přidejte nové umístění. V poli **odkazy** vyberte konfiguraci formátu **Aktivity importu / exportu aktivity**, kterou jste předtím vytvořili. Tento postup slouží k přidání nového záznamu cílového souboru pro odkaz.

1. V poli **název** zadejte název cíle souboru.
2. V poli **Název souboru** vyberte název **Výstupního souboru Excel** coby součást formátu souboru aplikace Excel.

Klepněte na tlačítko **Nastavení** pro nový záznam cíle. Potom můžete v dialogovém okně **nastavení cíle** provést následující kroky.

1. Na kartě **Power BI** nastavte možnost **Povoleno** na **Ano**.
2. V poli **SharePoint** vyberte typ dokumentu **Sdílené**, který jste vytvořili dříve.

## <a name="schedule-execution-of-the-configured-er-format"></a>Naplánujte provedení konfigurovaného ER formátu
1. Na stránce **Konfigurace** (**Správa organizace** &gt; **Elektronické vykazování** &gt; **Konfigurace**) zaškrtněte ve stromu konfigurace **Aktivity importu / exportu** konfiguraci, kterou jste předtím vytvořili.
2. Změňte stav verze 1.1 z **Koncept** na **dokončeno**, abyste tento formát zpřístupnili pro používání.

    [![Konfigurace aktivit importu/exportu na stránce Konfigurace.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Vyberte dokončenou verzi konfigurace **Aktivity importu / exportu** a poté klepněte na položku **spustit**. Všimněte si, že konfigurovaný cíl se aplikuje na výstupní výsledek vytvořený ve formátu aplikace Excel.
4. Nastavte možnost **Dávkové zpracování** na **Ano**, čímž spustíte tuto sestavu v bezobslužném režimu.
5. Klepněte na tlačítko **Opakování**, abyste mohli naplánovat požadované opakování spuštění této dávky. Opakování definuje, jak často se budou aktualizovaná data přesouvat do Power BI.

    [![Dialogové okno parametrů elektronického výkaznictví.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Po konfiguraci najdete ER sestavy spuštění úlohy na stránce **Dávkové úlohy** (**Správa systému &gt; Dotazy &gt; Dávkové úlohy**).

    [![Stránka dávkových úloh.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Při prvním spuštění této úlohy cíl vytvoří nový soubor Excel s názvem konfigurovaným do vybrané složky služby SharePoint. Při každém dalším spuštění úkolu cíl vytvoří novou verzi souboru aplikace Excel.

    [![Nová verze souboru aplikace Excel.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Vytvořte sadu dat Power BI s použitím výstupního výsledku ER formátu
1. Přihlaste se k Power BI a buď otevřete existující skupinu Power BI (pracovní prostor) nebo vytvořte novou skupinu. Klikněte na **Přidat** v části **Soubory** v oddílu **Importovat nebo připojit k datům** nebo klikněte na znaménko plus (**+**) vedle položky **Datové sady** v levém podokně.

    [![Vytváření sady dat.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Vyberte možnost **SharePoint – týmová pracoviště** a zadejte cestu serveru SharePoint Server, kterou používáte (v našem příkladu `https://ax7partner.litware.com`).
3. Přejděte do složky **/Shared Documents/GER data/PowerBI** a vyberte soubor aplikace Excel, který jste vytvořili jako zdroj dat pro novou sadu dat Power BI.

    [![Výběr souboru aplikace Excel.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Klepněte na položku **Připojit** a poté klepněte na položku **Import**. Vytvoří se nová sada dat na základě vybraného souboru aplikace Excel. Sadu dat lze také automaticky přidávat do nově vytvořeného řídicího panelu.

    [![Sada dat v řídicím panelu.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Konfigurujte naplánování obnovy pro tuto sadu dat, abyste si vynutili periodické aktualizace. Pravidelné aktualizace umožňují využití nových obchodních dat, která vznikají při pravidelném spouštění sestavy ER prostřednictvím nových verzí souboru aplikace Excel, které se vytváří na serveru SharePoint.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Vytvoření sestavy Power BI pomocí nové sady dat
1. Klikněte na tlačítko **Podrobnosti importu a exportu** sady dat Power BI, kterou jste vytvořili.
2. Nakonfigurujte vizualizaci. Vyberte například vizualizaci **Plná mapa** a proveďte její konfiguraci následujícím způsobem:

    - Přiřaďte sadu dat **CountryOrigin** do pole **Umístění** vizualizace mapy.
    - Přiřaďte sadu dat **Množství** do pole **Sytost barvy** vizualizace mapy.
    - Přidejte pole sad dat **aktivity** a **Rok** k polím **Filtry** kolekce vizualizace map.

3. Uložte sestavu Power BI jako **sestavu podrobností o importu a exportu**.

    [![Sestava podrobností o Importu a exportu.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Všimněte si, že mapa zobrazí země/oblasti, které jsou uvedeny v souboru Excel (Rakousko a Švýcarsko v tomto příkladu) Tyto země/oblasti se vybarví, aby zobrazily podíl fakturovaných částek pro každou z nich.

4. Aktualizujte seznam transakcí v systému Intrastat. Byla přidána transakce exportu, která pochází z Itálie.

    [![Seznam transakcí systému Intrastat.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Počkejte do dalšího plánovaného spuštění ER sestavy a další plánované aktualizace sady dat Power BI. Potom zkontrolujte sestavu Power BI (vyberte pro zobrazení pouze transakcí importu). Aktualizovaná mapa nyní zobrazuje Itálii.

    [![Aktualizovaná mapa.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Přístup k sestavě Power BI ve Finance
Nastavení integrace s modulem Power BI. Další informace naleznete v části [Konfigurace integrace Power BI pro pracovní prostory](configure-power-bi-integration.md).

1. Na stránce pracovního prostoru **Elektronické výkaznictví**, která podporuje integraci Power BI (**Správa organizace** &gt; **Pracovní prostory** &gt; **Pracovní prostor elektronického vykazování**) klikněte na tlačítko **Možnosti** &gt; **Otevřít sestavu katalogu**.
2. Vyberte **Podrobnosti Importu a exportu sestavy** Power BI, kterou jste vytvořili, aby se tato sestava zobrazila jako položka akcí na vybrané stránce.
3. Kliknutím na položku akce otevřete stránku se sestavami, které jste navrhli v Power BI.

    [![Sestava podrobností o Importu a exportu navržených v Power BI.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Další prostředky

[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
