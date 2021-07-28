---
title: Návrh formátu ER pro generování zprávy ve formátu Excel s vloženými obrázky v záhlaví nebo zápatí stránky
description: Toto téma vysvětluje, jak používat elektronické výkaznictví (ER) ke generování obchodních dokumentů, které mají obrázky a tvary vložené do záhlaví nebo zápatí stránky.
author: NickSelin
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e67c10ecb9f297d1855a55431cd07c53ee87d40a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361376"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Návrh formátu ER pro generování zprávy ve formátu Excel s vloženými obrázky v záhlaví nebo zápatí stránky

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje, jak může uživatel v roli administrátora systému nebo v role funkčního konzultanta elektronického výkaznictví provádět tyto úkoly:

- Konfigurace parametrů pro rámec [elektronického výkaznictví (ER)](general-electronic-reporting.md).
- Importujte [konfigurace](general-electronic-reporting.md#Configuration) ER, které jsou [poskytnuty](general-electronic-reporting.md#Provider) společností Microsoft a používají se ke generování [faktur s volným textem](../../../finance/accounts-receivable/create-free-text-invoice-new.md) na základě [šablony](er-fillable-excel.md#excel-file-component) ve formátu Microsoft Excel.
- Vytvoření [vlastní (odvozené)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) verze konfigurace standardního formátu ER od společnosti Microsoft.
- Upravte konfiguraci vlastního formátu ER tak, aby generovala sestavu faktury s volným textem, která má v zápatí obrázek loga společnosti.

Postupy v tomto tématu lze provést ve společnosti **USMF**. Není nutné žádné kódování. Před přihlášením je také nutné stáhnout a uložit následující soubor.

| popis        | Název souboru |
|--------------------|-----------|
| Obrázek loga společnosti | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Obsah

- [Konfigurace právnické osoby.](#ConfigureLegalEntity)
- [Konfigurace architektury ER](#ConfigureFramework)

    - [Konfigurace parametrů ER](#ConfigureParameters)
    - [Aktivace poskytovatele konfigurace ER](#ActivateProvider)

        - [Kontrola seznamu poskytovatelů konfigurace ER](#ReviewProvidersList)
        - [Přidání nového poskytovatele konfigurace ER](#AddProvider)
        - [Aktivace nového poskytovatele konfigurace ER](#ActivateAddedProvider)

- [Import standardních konfigurací formátu ER](#ImportERSolution1)

    - [Import standardních konfigurací ER](#ImportERFormat)
    - [Kontrola importovaných konfigurací ER](#ReviewImportedERSolution)

- [Tisk faktury s volným textem pomocí standardního formátu ER](#PrintInvoice1)

    - [Nastavení správy tisku](#ConfigurePrintManagement1)
    - [Tisk volné faktury](#ProcessInvoice1)

- [Přizpůsobení standardního formátu ER](#CustomizeProvidedFormat)

    - [Vytvoření vlastního formátu](#DeriveProvidedFormat)
    - [Úprava vlastního formátu](#ConfigureDerivedFormat)
    - [Označení vlastního formátu jako spustitelného](#MarkFormatRunnable)

- [Tisk faktury s volným textem pomocí vlastního formátu ER](#PrintInvoice2)

    - [Nastavení správy tisku](#ConfigurePrintManagement2)
    - [Tisk volné faktury](#ProcessInvoice2)

- [Další prostředky](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Konfigurace právnické osoby

1. Přejděte do části **Správa organizace** \> **Organizace** \> **Právnické osoby**.
2. Na stránce **Právnické osoby** na pevné záložce **Obrázek loga společnosti sestavy** vyberte **Změnit**.
3. V dialogovém okně **Vybrat soubor obrázku, který chcete nahrát** vyberte **Procházet** a vyberte soubor **Company logo.png**, který jste stáhli dříve.
4. Vyberte **Uložit** a poté zavřete stránku **Právnické osoby**.

![Obrázek loga společnosti vybraný na stránce Právnické osoby.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurace rámce ER

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER, abyste mohli začít používat rámec ER k navrhování vlastních verzí standardního formátu ER.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurace parametrů ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.
4. Na kartě **Přílohy** natavte následující parametry:

    - V poli **Konfigurace** vyberte pro společnost **USMF** typ **Soubor**.
    - V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.

Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví. Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**. Než začnete přidávat nebo upravovat konfigurace elektronického výkaznictví, musíte proto aktivovat poskytovatele konfigurace elektronického výkaznictví v pracovním prostoru **Elektronické výkaznictví**.

> [!NOTE]
> Pouze vlastník konfigurace elektronického výkaznictví může konfiguraci upravovat. Konfiguraci elektronického výkaznictví můžete upravovat teprve poté, co je příslušná konfigurace elektronického výkaznictví aktivována v pracovním prostoru **Elektronické výkaznictví**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL. Zkontrolujte obsah této stránky. Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#AddProvider), přeskočte.

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Přidání nového poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.
4. Do pole **Název** zadejte **Litware, Inc.**
5. Do pole **Internetová adresa** zadejte `https://www.litware.com`.
6. Zvolte možnost **Uložit**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivace nového poskytovatele konfigurace ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.

Další informace o poskytovatelích konfigurací ER naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Import standardních konfigurací formátu ER

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Import standardních konfigurací ER

Chcete-li přidat standardní konfigurace ER do aktuální instance systému Dynamics 365 Finance, musíte je importovat z [úložiště](general-electronic-reporting.md#Repository) ER, jež je pro tuto instanci nakonfigurováno.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Chcete-li zobrazit seznam úložišť pro poskytovatele **Microsoft**, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.
3. Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**. Pokud budete vyzváni k autorizaci pro připojení ke službě [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), postupujte podle pokynů k autorizaci.
4. Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **Faktura s volným textem (Excel)**.
5. Na záložce s náhledem **Verze** vyberte nejnovější verzi (např. **240.112**) vybrané konfigurace formátu ER.
6. Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.

![Import standardních konfigurací ER na stránce úložiště konfigurace.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Kontrola importovaných konfigurací ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte **Model faktury**.
4. Kromě vybraného formátu ER **Faktura s volným textem (Excel)** byly importovány další požadované konfigurace ER. Ujistěte se, že ve stromu konfigurací jsou k dispozici následující konfigurace ER:

    - **Model faktury** – Tato konfigurace obsahuje komponentu ER [datový model](general-electronic-reporting.md#data-model-and-model-mapping-components), jež představuje datovou strukturu podnikové domény faktury.
    - **Mapování modelu faktury** – Tato konfigurace obsahuje komponentu ER [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components), jež popisuje, jak se datový model vyplněn za chodu daty z aplikace.
    - **Faktura s volným textem (Excel)** – Tato konfigurace obsahuje [formát](general-electronic-reporting.md#FormatComponentOutbound) a mapování formátu komponent ER. Komponenta formátu určuje rozložení sestavy na základě šablony ve formátu Excel. Komponenta mapování formátu obsahuje zdroj dat modelu a určuje, jak se tento zdroj dat používá k vyplnění rozvržení sestavy za chodu.

![Importované konfigurace elektronického výkaznictví na stránce konfigurace.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Tisk faktury s volným textem pomocí standardního formátu ER

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Nastavení správy tisku

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Faktura s volným textem** vyberte fakturu **FTI-00000002** a poté na panelu akcí na kartě **Faktura** ve skupině **Správa tisku** vyberte **Správa tisku**.
3. Na stránce **Nastavení správy tisku** ve stromu vlevo rozbalte **Modul – pohledávky \> Dokumenty \> Faktura s volným textem** a potom vyberte položku **Originál \<Default\>**.
4. V poli **Formát zprávy** vyberte **Faktura s volným textem (Excel)**.
5. Vyberte tlačítko **Esc** k opuštění stránky **Nastavení správy tisku** a vraťte se na stránku **Faktura s volným textem**.

![Nastavení správy tisku pro fakturu s volným textem ve standardním formátu ER na stránce Nastavení správy tisku.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Tisk volné faktury

1. Na stránce **Faktura s volným textem** zkontrolujte, že je stále vybraná faktura **FTI-00000002**, a poté na panelu akcí na kartě **Faktura** ve skupině **Dokument** vyberte **Tisk** \> **Vybráno**.
2. Stáhněte si vygenerovanou fakturu ve formátu Excel a otevřete ji pro náhled.
3. Všimněte si, že v souladu se strukturou šablony aplikace Excel pro poskytovaný formát ER obsahuje zápatí stránky vygenerované faktury informace o aktuálním čísle stránky a celkovém počtu stránek v sestavě.

![Vygenerovaná faktura s volným textem.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Přizpůsobení standardního formátu ER

Například v této části můžete použít konfigurace ER, které poskytuje společnost Microsoft, ke generování faktury s volným textem ve formátu Excel. Musíte však přidat přizpůsobení, aby se obrázek loga společnosti umístil do zápatí stránky vygenerovaných faktur.

V tomto případě musíte jako zástupce společnosti Litware, Inc., vytvořit (odvodit) novou konfiguraci formátu ER, která je založena na konfiguraci **Faktura s volným textem (Excel)**.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Vytvoření vlastního formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury** a vyberte možnost **Faktura s volným textem (Excel)**. Společnost Litware, Inc., použije importovanou verzi (například **240.112**) této konfigurace formátu ER jako základ pro vlastní verzi.
3. Výběrem možnosti **Vytvořit konfiguraci** otevřete rozbalovací dialogovou nabídku. Tuto dialogovou nabídku použijte k vytvoření nové konfigurace pro vlastní formát platby.
4. Ve skupině polí **Nový** vyberte možnost **Odvodit z názvu: Faktura s volným textem (Excel), Microsoft**.
5. Do pole **Název** zadejte **Faktura s volným textem (Excel) vlastní**.
6. Vyberte **Vytvořit konfiguraci**.

![Vytvoření konfigurace pro vlastní formát platby v rozevíracím dialogovém okně Vytvořit konfiguraci.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Verze 240.112.1 formátu ER **Faktura s volným textem (Excel) vlastní** je vytvořena. Tato verze je ve [stavu](general-electronic-reporting.md#component-versioning) **Konceptu** a je editovatelná. Aktuální obsah vašeho vlastního formátu ER odpovídá obsahu formátu poskytnutého společností Microsoft.

![Nová vytvořená verze konfigurace formátu ER na stránce Konfigurace.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Úprava vlastního formátu

Nakonfigurujte svůj vlastní formát tak, aby byl obrázek loga společnosti vložen do zápatí na každé stránce sestavy.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a vyberte možnost **Faktura s volným textem (Excel) vlastní**.
3. Na záložce s náhledem **Verze** vyberte jako požadovanou verzi vybrané konfigurace **240.112.1**.
4. Vyberte možnost **Návrhář**.
5. Na stránce **Návrhář formátu** vyberte možnost **Zobrazit podrobnosti**. Zobrazí se další informace o prvcích formátu.
6. Rozbalte a zkontrolujte následující prvky:

    - Prvek **Faktura s volným textem** typu **Excel**. Tento prvek se používá ke generování faktury ve formátu sešitu aplikace Excel.
    - Prvek **Faktura s volným textem \\ Faktura** typu **List**. Tento prvek se používá ke generování listu vygenerovaného sešitu aplikace Excel.
    - Prvek **Faktura s volným textem \\ Faktura \\ Zápatí** typu **Zápatí**. Tento prvek se používá k vyplnění zápatí faktury.

7. Vyberte prvek **Faktura s volným textem \\ Faktura \\ Zápatí**.

    ![Prvek zápatí v návrháři operací ER.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Každé zápatí stránky vygenerované faktury obsahuje informace o aktuálním čísle stránky a celkovém počtu stránek v sestavě. Jak vidíte, prvek **Faktura s volným textem \\ Faktura \\ Zápatí** neobsahuje žádné podřízené prvky. Šablona aplikace Excel, která se používá, je proto nakonfigurována tak, aby zobrazovala podrobnosti stránkování ve středu zápatí každé sestavy.

8. Vyberte **Přidat** a poté vyberte typ **Excel \\ Obrázek** prvky formátu, který přidáváte:

    1. V **Zarovnání** vyberte **Doprava**.
    2. V poli **Měřítko výšky** vyberte **Relativní**.
    3. Do pole **Měřítko v procentech** zadejte **70**.
    4. Vyberte **OK**.

        > [!NOTE]
        > Prvek **Excel \\ Obrázek** se používá k přidání obrázku loga společnosti a jeho zarovnání na pravou stranu zápatí stránky.

    ![Vlastnosti prvku Obrázek v dialogovém okně Vlastnosti komponenty.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Ve stromu struktury formátu vlevo vyberte prvek **Obrázek**, který jste právě přidali, a poté na kartě **Mapování** rozbalte zdroj dat **model**.
10. Rozbalte **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** a potom vyberte pole zdroje dat **model.InvoiceBase.CompanyInfo.Logo**. Pole zdroje dat typu [Kontejner](er-formula-supported-data-types-composite.md#container) vystavuje obrázek loga společnosti jako mediální obsah.
11. Vyberte možnost **vazba**. Prvek formátu **Obrázek** je nyní svázán s polem zdroje dat **model.InvoiceBase.CompanyInfo.Logo**. Proto bude za běhu vložen obrázek loga společnosti do zápatí vygenerovaných faktur.

    ![Prvek formátu svázaný s polem zdroje dat model.InvoiceBase.CompanyInfo.Logo v návrháři operací ER.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Vyberte **Uložit** a poté zavřete stránku **Návrhář**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Označení vlastního formátu jako spustitelného

Protože máte vytvořenou první verzi vlastního formátu a ten je ve stavu **Koncept**, můžete formát pro testovací účely spustit. Chcete-li sestavu spustit, zpracujte platbu dodavateli pomocí způsobu platby, která odkazuje na váš vlastní formát ER. Ve výchozím nastavení jsou při volání formátu ER z aplikace [zvažovány](general-electronic-reporting.md#component-versioning) pouze verze se stavem **Dokončeno** nebo **Sdíleno**. Toto chování pomáhá zabránit použití formátů ER s nedokončenými návrhy. Pro zkušební účely však můžete aplikaci přinutit, aby použila verzi formátu ER ve stavu **Koncept**. Pokud při testu zjistíte, že je třeba provést nějaké změny, můžete následně aktuální verzi formátu upravit. Další informace naleznete v tématu [Použitelnost](electronic-reporting-destinations.md#applicability).

Chcete-li použít koncept formátu ER, musíte příslušný formát ER explicitně označit.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.
4. Vyberte **Upravit**, aby bylo možné aktuální stránku upravovat, a poté ve stromu konfigurací v levém podokně vyberte možnost **Faktura s volným textem (Excel) vlastní**.
5. U možnosti **Spustit koncept** nastavte hodnotu **Ano**.

![Označení vlastního formátu jako spustitelného na stránce Konfigurace.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Tisk faktury s volným textem pomocí vlastního formátu ER

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Nastavení správy tisku

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Faktura s volným textem** vyberte fakturu **FTI-00000002** a poté na panelu akcí na kartě **Faktura** ve skupině **Správa tisku** vyberte **Správa tisku**.
3. Na stránce **Nastavení správy tisku** ve stromu vlevo rozbalte **Modul – pohledávky** \> **Dokumenty** \> **Faktura s volným textem** a potom vyberte položku **Originál** **\<Default\>**.
4. V poli **Formát zprávy** vyberte **Faktura s volným textem (Excel) vlastní**.
5. Vyberte klávesu **Esc** k opuštění stránky **Nastavení správy tisku** a vraťte se na stránku **Faktura s volným textem**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Tisk volné faktury

1. Na stránce **Faktura s volným textem** zkontrolujte, že je stále vybraná faktura **FTI-00000002**, a poté na panelu akcí na kartě **Faktura** ve skupině **Dokument** vyberte **Tisk** \> **Vybráno**.
2. Stáhněte si vygenerovanou fakturu ve formátu Excel a otevřete ji pro náhled.
3. Všimněte si, že v souladu se strukturou vlastního formátu ER obsahuje zápatí stránky vygenerované faktury kromě informací o stránkování sestavy také obrázek loga společnosti.

![Vygenerovaná faktura s volným textem s obrázkem loga společnosti v zápatí stránky.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Další prostředky

- [Návrh konfigurace pro generování dokumentů ve formátu Excel](er-fillable-excel.md)
- [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)
