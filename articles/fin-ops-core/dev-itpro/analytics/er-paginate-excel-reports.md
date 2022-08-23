---
title: Návrh formátu ER pro stránkování generovaného dokumentu ve formátu aplikace Excel
description: Tento článek vysvětluje, jak navrhnout formát elektronického výkaznictví (ER), který stránkuje generovaný dokument v aplikaci Microsoft Excel.
author: kfend
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner
ms.openlocfilehash: e4a34dffda9e9b95f5d6c7ee382723663817ec6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284994"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Návrh formátu ER pro stránkování generovaného dokumentu ve formátu aplikace Excel

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak může uživatel s rolí Správce systému nebo Funkční konzultant elektronického výkaznictví konfigurovat formát [elektronického vykazování (ER)](general-electronic-reporting.md) pro generování odchozích dokumentů v aplikaci Microsoft Excel a spravovat stránkování dokumentů.

V tomto příkladu upravíte formát ER poskytovaný společností Microsoft, který se používá k tisku kontrolní sestavy, když je [generována](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) deklarace Intrastat. Tato sestava vám umožňuje sledovat vykázané transakce Intrastat. Vaše úpravy vám umožní spravovat stránkování generovaných kontrolních sestav.

Postupy v tomto článku lze provést ve společnosti **DEMF**. Není nutné žádné kódování. Před přihlášením je také nutné stáhnout a uložit následující soubory.

| popis       | Název souboru |
|-------------------|-----------| 
| Šablona sestavy 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Šablona sestavy 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k návrhu vlastní verze standardního formátu ER.

## <a name="import-the-standard-er-format-configuration"></a>Import standardní konfigurace formátu ER

Postupujte podle kroků uvedených v části [Import standardní konfigurace formátu ER](er-quick-start2-customize-report.md#ImportERSolution1) a přidejte standardní konfigurace ER do vaší aktuální instance Dynamics 365 Finance. Importujte verzi **1.9** z konfigurace formátu **Sestava Intrastat**. Základní verze 1 základní konfigurace **Model Intrastat** se automaticky importuje z úložiště.

## <a name="customize-the-standard-er-format"></a>Přizpůsobení standardního formátu ER

### <a name="create-the-custom-er-format"></a>Vytvoření vlastního formátu ER

V tomto scénáři jste zástupcem společnosti Litware, Inc., která je aktuálně vybrána jako aktivní poskytovatel konfigurace ER. Musíte vytvořit novou konfiguraci formátu ER a jako základ použijete konfiguraci **Sestava Intrastat**.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model Intrastat** a poté vyberte možnost **Sestava Intrastat**. Společnost Litware, Inc. použije verzi 1.9 této konfigurace formátu ER jako základ pro vlastní verzi.
3. Výběrem možnosti **Vytvořit konfiguraci** otevřete rozbalovací dialogovou nabídku. Tuto dialogovou nabídku můžete použít k vytvoření nové konfigurace pro vlastní formát platby.
4. Ve skupině polí **Nový** vyberte možnost **Odvodit z názvu: Sestava Intrastat, Microsoft**.
5. Do pole **Název** zadejte **Sestava Intrastat Litware**.
6. Vytvořte nový formát zvolením položky **Vytvořit konfiguraci**.

Vytvoří se verze 1.9.1 konfigurace formátu ER **Sestava Intrastat Litware**. Tato verze je ve stavu **Koncept** a je editovatelná. Aktuální obsah vašeho vlastního formátu ER odpovídá obsahu formátu poskytnutého společností Microsoft.

### <a name="make-the-custom-format-runnable"></a>Označení vlastního formátu jako spustitelného

Nyní, když máte vytvořenou první verzi vlastního formátu a ten je ve stavu **Koncept**, můžete formát pro testovací účely spustit. Chcete-li sestavu spustit, zpracujte platbu dodavateli pomocí způsobu platby, která odkazuje na váš vlastní formát ER. Ve výchozím nastavení jsou při volání formátu ER z aplikace zvažovány pouze verze se stavem **Dokončeno** nebo **Sdíleno**. Toto chování pomáhá zabránit použití formátů ER s nedokončenými návrhy. Pro zkušební účely však můžete aplikaci přinutit, aby použila verzi formátu ER ve stavu **Koncept**. Pokud při testu zjistíte, že je třeba provést nějaké změny, můžete následně aktuální verzi formátu upravit. Další informace naleznete v tématu [Použitelnost](electronic-reporting-destinations.md#applicability).

Chcete-li použít koncept formátu ER, musíte příslušný formát ER explicitně označit.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.
4. Je-li třeba vyberte možnost **Upravit**, má-li být aktuální stránka editovatelná.
5. Ve stromu konfigurace v levém podokně vyberte **Sestava Intrastat Litware**.
6. Nastavte možnost **Spustit koncept** na **Ano** a pak vyberte **Uložit**.

    ![Možnost Spustit koncept na stránce Konfigurace.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Nastavení používání vlastního formátu ER u parametrů zahraničního obchodu

Podle následujících kroků nakonfigurujte parametry zahraničního obchodu, abyste mohli používat vlastní formát.

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Parametry zahraničního obchodu**.
2. Na kartě **Parametry zahraničního obchodu** na záložce **Elektronické výkaznictví** vyberte v poli **Mapování formátu souboru** hodnotu **Sestava Intrastat Litware**.
3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat Litware**.
4. Zvolte možnost **Uložit**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Konfigurace používání stažené šablony sestavy u vlastního formátu

### <a name="review-the-first-downloaded-excel-template"></a>Zkontrolujte první staženou šablonu aplikace Excel

1. V desktopové aplikaci Excel otevřete soubor šablony **ERIntrastatReportDemo1.xlsx**, který jste stáhli dříve.
2. Ověřte, že šablona obsahuje pojmenované rozsahy pro vytvoření sekcí záhlaví sestavy, detailů sestavy a zápatí sestavy v generovaných dokumentech.

    ![Rozvržení šablony Excel 1 v desktopové aplikaci.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Nahraďte aktuální šablonu aplikace Excel ve vlastním formátu ER

Do vlastního formátu ER musíte přidat novou šablonu aplikace Excel.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model Intrastat** \> **Sestava Intrastat** a vyberte konfiguraci **Sestava Intrastat Litware**.
3. Vyberte možnost **Návrhář**.
4. Na stránce **Návrhář formátu** v podokně akcí vyberte **Zobrazit detaily**.
5. Ujistěte se, že je vybrána komponenta kořenového formátu **Intrastat: Excel** a poté v podokně akcí na kartě **Import** ve skupině **Import** vyberte **Aktualizovat z Excelu**.
6. V dialogovém okně **Aktualizovat z Excelu** vyberte **Aktualizovat šablonu**.
7. V dialogovém okně **Otevřít** vyhledejte a vyberte soubor **ERIntrastatReportDemo1.xlsx**, který jste stáhli dříve, a poté vyberte **Otevřít**.
8. Vyberte **OK**.
9. Zvolte možnost **Uložit**.

![Struktura formátu v návrháři formátu ER po přidání nové šablony aplikace Excel.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Změna datové vazby k zobrazení popisu položky ve vygenerované sestavě

1. Na stránce **Návrhář formátu** vyberte kartu **Mapování.**
2. Rozbalte uzel **Intrastat** \> **Řádky sestavy** a vyberte komponentu **Kód zboží**.
3. Vyberte možnost **Upravit vzorec**.
4. Změňte vzorec vazby z `@.CommodityCode` na `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Zvolte možnost **Uložit**.

![Konfigurovaná vazba pro zobrazení popisu položky v návrháři formátu ER.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Generování kontrolní sestavy prohlášení Intrastat

Nejprve se ujistěte, že máte transakce Intrastat pro vykazování ve stránce **Intrastat**.

![Transakce na stránce Intrastat.](./media/er-paginate-excel-reports-transactions1.gif)

Poté pomocí vlastního formátu ER vygenerujte kontrolní sestavu prohlášení Intrastat.

1. Přejděte na **Daň** \> **Deklarace** \> **Zahraniční obchod** \> **Intrastat**.
2. Na stránce **Intrastat** v podokně akcí vyberte **Výstup** \> **Sestava**.
3. V dialogovém okně **Sestava Intrastat** spusťte sestavu takto:

    1. Pole **Od data** a **Do data** nastavte tak, aby zahrnuly konkrétní transakce Intrastat do sestavy.
    2. Nastavte možnost **Generovat soubor** na **Ne**.
    3. Nastavte možnost **Generovat sestavu** na **Ano**.
    4. Vyberte **OK**.

4. Stáhněte a uložte vygenerovaný dokument.
5. Otevřete dokument v aplikaci Excel a zkontrolujte jeho obsah.

    ![Vygenerovaný dokument aplikace Excel v desktopové aplikaci.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Konfigurace vlastního formátu pro stránkování generovaných dokumentů

### <a name="review-the-second-downloaded-excel-template"></a>Zkontrolujte druhou staženou šablonu aplikace Excel

1. V desktopové aplikaci Excel otevřete soubor šablony **ERIntrastatReportDemo2.xlsx**, který jste stáhli dříve.
2. Porovnejte tuto šablonu s šablonou **ERIntrastatReportDemo1.xlsx** šablonu a ověřte, že obsahuje několik nových názvů aplikace Excel k vytváření a vyplňování sekcí specifických pro stránky ve vygenerovaných dokumentech:

    - Rozsah **ReportPageHeader** se přidá pro vytváření záhlaví stránek.
    - Rozsah **ReportPageFooter** se přidá pro vytváření zápatí stránek.
    - Buňka **ReportPageFooter\_PageLines** je konfigurována tak, aby zobrazovala počet transakcí na stránku.
    - Buňka **ReportPageFooter\_PageAmount** je konfigurována tak, aby zobrazovala celkové množství transakcí na stránku.
    - Buňka **ReportPageFooter\_PageWeight** je konfigurována tak, aby zobrazovala celkovou hmotnost transakcí na stránku.
    - Buňka **ReportPageFooter\_RunningCounterLines** je konfigurována tak, aby zobrazovala průběžný čítač transakcí od začátku sestavy přes aktuální stránku.
    - Buňka **ReportPageFooter\_RunningTotalAmount** je konfigurována tak, aby zobrazovala množství průběžného součtu všech transakcí od začátku sestavy přes aktuální stránku.
    - Buňka **ReportPageFooter\_RunningTotalWeight** je konfigurována tak, aby zobrazovala hmotnost průběžného součtu transakcí od začátku sestavy přes aktuální stránku.

    ![Rozvržení šablony Excel 2 v desktopové aplikaci.](./media/er-paginate-excel-reports-template2a.gif)

    Buňka **CommodityCode** této šablony je nakonfigurována tak, aby zabalila text buňky. Protože řádek podrobností transakce je konfigurován tak, aby se automaticky přizpůsobil výšce řádku, musí se výška celého řádku automaticky změnit, když se text v buňce **CommodityCode** zabalí.

    ![Buňka CommodityCode je konfigurována tak, aby zabalila text buňky.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Opakujte nahrazení aktuální šablony aplikace Excel ve vlastním formátu ER

1. Postupujte podle pokynů v části [Nahraďte aktuální šablonu aplikace Excel ve vlastním formátu ER](#replace-template) tohoto článku. V kroku 7 však vyberte soubor **ERIntrastatReportDemo2.xlsx**.
2. Na stránce **Návrhář formátu** rozbalte uzel **Intrastat**.
3. Pojmenujte komponenty formátu [rozsahu](er-fillable-excel.md#range-component), které byly přidány do upravitelného formátu ER za účelem synchronizace struktury se strukturou použité šablony aplikace Excel:

    1. Vyberte komponentu **Rozsah**, která je asociována s názvem aplikace Excel **ReportPageHeader**.
    2. Na kartě **Formát** v poli **Název** zadejte **Záhlaví stránky sestavy**.
    3. Vyberte komponentu **Rozsah**, která je asociována s názvem aplikace Excel **ReportPageFooter**.
    4. Na kartě **Formát** v poli **Název** zadejte **Zápatí stránky sestavy**.

4. Zvolte možnost **Uložit**.

![Struktura formátu v návrháři formátu ER po nahrazení šablony aplikace Excel.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Chcete-li implementovat stránkování dokumentu, změňte strukturu formátu

1. Na stránce **Návrhář formátu** ve stromu formátu v levém podokně vyberte kořenovou komponentu **Intrastat**.
2. Vyberte **přidat**.
3. V dialogovém okně **Přidat** vyberte komponentu [Strana](er-fillable-excel.md#page-component) ve skupině komponent **Excel**.
4. V dialogovém okně **Vlastnosti komponenty** do pole **Název** zadejte **Stránka sestavy**. Pak vyberte **OK**.
5. Chcete-li použít komponentu **Záhlaví stránky sestavy** jako záhlaví stránky na každé generované stránce, postupujte takto:

    1. Vyberte komponentu **Záhlaví stránky sestavy** a poté vyberte **Vyjmout**.
    2. Vyberte komponentu **Stránka sestavy** a poté vyberte **Vložit**.
    3. Rozbalte **Stránku sestavy**.
    4. Aby komponenta **Strana** musela [považovat](er-fillable-excel.md#page-component-structure) tento rozsah za záhlaví stránky, vyberte **Záhlaví stránky sestavy**, a potom na kartě **Formát** v poli **Směr replikace** vyberte hodnotu **Žádná replikace**.

6. Chcete-li stránkovat generovaný dokument, aby byl zohledněn obsah na řádcích sestavy, postupujte takto:

    1. Vyberte komponentu **Řádky sestavy** a poté vyberte **Vyjmout**.
    2. Vyberte komponentu **Stránka sestavy** a poté vyberte **Vložit**.

7. Chcete-li vložit zápatí sestavy za řádky sestavy, ale před zápatí závěrečné stránky, postupujte takto:

    1. Vyberte komponentu **Záhlaví sestavy** a poté vyberte **Vyjmout**.
    2. Vyberte komponentu **Stránka sestavy** a poté vyberte **Vložit**.

8. Chcete-li použít komponentu **Zápatí stránky sestavy** jako zápatí stránky na každé generované stránce, postupujte takto:

    1. Vyberte komponentu **Zápatí stránky sestavy** a poté vyberte **Vyjmout**.
    2. Vyberte komponentu **Stránka sestavy** a poté vyberte **Vložit**.
    3. Aby komponenta **Strana** musela [považovat](er-fillable-excel.md#page-component-structure) tento rozsah za zápatí stránky, vyberte **Zápatí stránky sestavy**, a potom na kartě **Formát** v poli **Směr replikace** vyberte hodnotu **Žádná replikace**.

![Struktura formátu v návrháři formátu ER po implementaci stránkování dokumentu.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Přidání zdrojů dat pro výpočet součtů zápatí stránky

Musíte konfigurovat nové zdroje dat pro výpočet celkového počtu stránek, průběžného čítače a průběžných celkových součtů, a zobrazit tyto údaje v sekci zápatí stránky. Doporučujeme k tomuto účelu použít zdroje dat funkce [shromažďování dat](er-data-collection-data-sources.md).

1. Na stránce **Návrhář formátu** vyberte kartu **Mapování.**
2. Vyberte možnost **Přidat kořen** a postupujte podle následujících kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Všeobecné** vyberte **Prázdný kontejner**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Prázdný kontejner“** v poli **Název** zadejte **Total** (Celkem).
    3. Vyberte **OK**.

3. Vyberte zdroj dat **Total**, vyberte **Přidat** a poté postupujte podle těchto kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Všeobecné** vyberte **Prázdný kontejner**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Prázdný kontejner“** v poli **Název** zadejte **Page** (Stránka).
    3. Vyberte **OK**.

4. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Všeobecné** vyberte **Prázdný kontejner**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Prázdný kontejner“** v poli **Název** zadejte **Running** (Průběžný).
    3. Vyberte **OK**.

5. Vyberte zdroj dat **Total.Page**, vyberte **Přidat** a poté postupujte podle těchto kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Amount** (Množství).
    3. V poli **Typ položky** vyberte **Reálný**.
    4. Nastavte možnost **Shromáždit všechny hodnoty** na **Ano**.
    5. Vyberte **OK**.

6. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Weight** (Hmotnost).
    3. V poli **Typ položky** vyberte **Reálný**.
    4. Nastavte možnost **Shromáždit všechny hodnoty** na **Ano**.
    5. Vyberte **OK**.

7. Vyberte zdroj dat **Total.Running**, vyberte **Přidat** a poté postupujte podle těchto kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Amount** (Množství).
    3. V poli **Typ položky** vyberte **Reálný**.
    4. Nastavte pole **Shromáždit všechny hodnoty** na **Ano**.
    5. Vyberte **OK**.

8. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Weight** (Hmotnost).
    3. V poli **Typ položky** vyberte **Reálný**.
    4. Nastavte pole **Shromáždit všechny hodnoty** na **Ano**.
    5. Vyberte **OK**.

9. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
    2. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Lines** (Řádky).
    3. V poli **Typ položky** vyberte **Celé číslo**.
    4. Nastavte pole **Shromáždit všechny hodnoty** na **Ano**.
    5. Vyberte **OK**.

10. Zvolte možnost **Uložit**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Přidání zdrojů dat pro řízení viditelnosti zápatí stránky

Pokud plánujete řídit viditelnost zápatí stránky, ale nechcete vložit zápatí na poslední stránku, pokud obsahuje transakce, nakonfigurujte nový zdroj dat pro výpočet požadovaného průběžného čítače.

1. Na stránce **Návrhář formátu** vyberte kartu **Mapování.**
2. Vyberte zdroj dat **Total.Running** a vyberte **Přidat**.
3. V dialogovém okně **Přidat zdroj dat** v části **Funkce** vyberte **Shromažďování dat**.
4. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **Lines2**.
5. V poli **Typ položky** vyberte **Celé číslo**.
6. Nastavte možnost **Shromáždit všechny hodnoty** na **Ano**.
7. Vyberte **OK**.
8. Zvolte možnost **Uložit**.

![Přidané zdroje dat v návrháři formátu ER.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Konfigurace shromažďování hodnot celkových součtů u vazeb

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Řádky sestavy** a vyberte vnořenou komponentu **Hodnota faktury**.
2. Vyberte možnost **Upravit vzorec**.
3. Změňte vzorec vazby z `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` na `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Kromě vložení hodnoty množství do buňky aplikace Excel pro každou iterovanou transakci tato vazba shromažďuje hodnotu ve zdroji dat **Total.Page.Amount** shromažďování dat.

4. Vyberte vnořenou komponentu **Weight**.
5. Vyberte možnost **Upravit vzorec**.
6. Změňte vzorec vazby z `@.'$RoundedWeight'` na `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Kromě vložení hodnoty hmotnosti do buňky aplikace Excel pro každou iterovanou transakci tato vazba shromažďuje hodnotu ve zdroji dat **Total.Page.Weight** shromažďování dat.

![Konfigurované vazby pro shromažďování hodnot celkových součtů v návrháři formátu ER.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Konfigurujte vazby tak, aby vyplňovaly součty zápatí stránky

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Zápatí stránky sestavy**, vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_PageAmount** Excelu, a poté postupujte takto:

    1. Ve stromu zdrojů dat v pravém podokně vyberte položku **Total.Page.Amount.Sum()**.
    2. Vyberte možnost **vazba**.
    3. Vyberte možnost **Upravit vzorec**.
    4. Aktualizujte vzorec na `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Argument této funkce musíte zadat jako **False** (nepravda), aby byla zachována shromážděná data pro aktuální stránku, protože tato data jsou potřebná k výpočtu průběžného celkového množství, celkového počtu řádků na stránce a průběžného čítače řádků.

2. Ve stromu formátu vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_PageWeight** Excelu, a poté postupujte takto:

    1. Ve stromu zdrojů dat v pravém podokně vyberte položku **Total.Page.Weight.Sum()**.
    2. Vyberte možnost **vazba**.
    3. Vyberte možnost **Upravit vzorec**.
    4. Aktualizujte vzorec na `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Konfigurace vyplňování průběžných součty stránky u vazeb

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Zápatí stránky sestavy**, vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_RunningTotalAmount** Excelu, a poté postupujte takto:

    1. Ve stromu zdrojů dat v pravém podokně vyberte položku **Total.Running.Amount.Collect()**.
    2. Vyberte možnost **vazba**.
    3. Vyberte možnost **Upravit vzorec**.
    4. Aktualizujte vzorec na `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > Operand `Total.Running.Amount.Sum(false)` vrací dříve shromážděné průběžné součty množství. Operand `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` vrací celkové množství aktuální stránky. Argument vnořené funkce druhého operandu musíte zadat jako **True** (pravda), aby bylo vynulováno shromažďování dat `Total.Page.Amount`, jakmile je tato hodnota vložena do průběžného celkového součtu `Total.Running.Amount`. Zadaný argument musí začít shromažďovat součet na další stránce od hodnoty 0 (nula).
    >
    > Funkce `Total.Running.Amount.Sum(false)` je volána pro zadání průběžného celkového množství do buňky **ReportPageFooter\_RunningTotalAmount** Excelu na aktuální stránce.

2. Ve stromu formátu vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_RunningTotalWeight** Excelu, a poté postupujte takto:

    1. Ve stromu zdrojů dat v pravém podokně vyberte položku **Total.Running.Weight.Collect()**.
    2. Vyberte možnost **vazba**.
    3. Vyberte možnost **Upravit vzorec**.
    4. Aktualizujte vzorec na `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Konfigurace vyplňování průběžného čítače stránky u vazeb

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Zápatí stránky sestavy** a vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_RunningCounterLines** Excelu.
2. Vyberte možnost **Upravit vzorec**.
3. Přidejte vzorec `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Tento vzorec vrací počet shromážděných hodnot množství za celou sestavu. Toto číslo se rovná počtu transakcí, které byly v aktuálním okamžiku iterovány. Současně vzorec shromažďuje vrácenou hodnotu **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Konfigurace vyplňování čítače zápatí stránky u vazeb

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Zápatí stránky sestavy** a vyberte vnořenou komponentu **Rozsah**, která odkazuje na buňku **ReportPageFooter\_PageLines** Excelu.
2. Vyberte možnost **Upravit vzorec**.
3. Přidejte vzorec `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Tento vzorec vypočítá počet transakcí na aktuální stránce jako rozdíl mezi počtem transakcí, které byly shromážděny v údaji **Total.Page.Amount.Result** za celou sestavu, a počtem transakcí, které byly v této fázi uloženy v údaji **Total.Running.Lines.Sum**. Protože počet transakcí pro aktuální stránku je uložen v údaji **Total.Running.Lines** ve vazbě komponenty **Rozsah**, která odkazuje na buňku **ReportPageFooter\_RunningCounterLines** Excelu, počet transakcí na aktuální stránce ještě není započítán. Tento rozdíl se tedy rovná počtu transakcí na aktuální stránce.

![Konfigurované vazby pro vyplňování čítače zápatí stránky v návrháři formátu ER.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Konfigurace viditelnosti komponenty

Viditelnost záhlaví a zápatí stránky na konkrétní stránce generovaného dokumentu můžete změnit tak, aby byly skryty následující prvky:

- Záhlaví stránky na první stránce, protože záhlaví sestavy již obsahuje názvy sloupců
- Záhlaví stránky na jakékoli stránce neobsahující transakce, které se vyskytnou na poslední stránce
- Zápatí stránky na jakékoli stránce neobsahující transakce, které se vyskytnou na poslední stránce

Chcete-li změnit viditelnost, aktualizujte vlastnost **Povoleno** komponent **Záhlaví stránky sestavy** a **Zápatí stránky sestavy**.

1. Na stránce **Návrhář formátu** ve stromu formátu rozbalte komponentu **Stránka sestavy**, vyberte vnořenou komponentu **Záhlaví stránky sestavy** a poté postupujte takto:

    1. Vyberte možnost **Upravit** pro pole **Povoleno**.
    2. Na stránce **Návrhář vzorců** v poli **Vzorec** zadejte následující výraz:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Ve stromu formátu vyberte vnořenou komponentu **Zápatí stránky sestavy** a poté postupujte takto:

    1. Vyberte možnost **Upravit** pro pole **Povoleno**.
    2. Na stránce **Návrhář vzorců** v poli **Vzorec** zadejte následující výraz:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Výraz `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` se používá k výpočtu počtu transakcí na aktuální stránce. Výraz `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` slouží k přidání počtu transakcí na aktuální stránce do kolekce dat, aby byla správně zpracována viditelnost zápatí na další stránce.
    >
    > Kolekci `Total.Running.Lines` zde nelze znovu použít, protože vlastnost **Povoleno** základní komponenty je zpracována až **poté**, co jsou zpracovány vazby vnořených komponent. Když je zpracována vlastnost **Povoleno**, je kolekce `Total.Running.Lines` již zvýšena o počet transakcí na aktuální stránce.

3. Zvolte možnost **Uložit**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Generování kontrolní sestavy prohlášení Intrastat (aktualizováno)

1. Zkontrolujte, že ve stránce **Intrastat** máte 24 transakcí. Opakujte kroky v části [Generování kontrolní sestavy prohlášení Intrastat](#generate-intrastat-control-report) tohoto článku a zkontrolujte vygenerovanou kontrolní sestavu.

    Všechny transakce jsou uvedeny na první stránce. Součty a čítače stránky se rovnají součtům a čítačům sestavy. Záhlaví stránky na první stránce je skryté, protože záhlaví sestavy již obsahuje názvy sloupců. Záhlaví a zápatí stránky na druhé stránce jsou skryté, protože tato stránka neobsahuje žádné transakce.

    ![Vygenerovaný dokument aplikace Excel v desktopové aplikaci.](./media/er-paginate-excel-reports-document2.gif)

2. Aktualizujte dvě transakce na stránce **Intrastat** změnou kódu **Číslo položky** z **D00006** na **L0010**. Všimněte si, že název produktu nové položky **Aktivní pár stereo reproduktorů** je delší než název produktu původní položky **Standardní reproduktor**. Tato situace si vynutí zalamování textu v odpovídající buňce generovaného dokumentu. Stránkování dokumentu a sčítání a počítání související se stránkováním je nyní nutné aktualizovat. Opakujte kroky v části [Generování kontrolní sestavy prohlášení Intrastat](#generate-intrastat-control-report) a zkontrolujte vygenerovanou kontrolní sestavu.

    Aktuálně jsou transakce prezentovány na dvou stránkách a součty a čítače stránek jsou správně vypočítány. Rozsah záhlaví stránky je správně na první stránce skryt a na druhé stránce je viditelný. Zápatí stránky je viditelné na obou stránkách, protože obsahují transakce.

    ![Aktualizovaný vygenerovaný dokument aplikace Excel v desktopové aplikaci.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Existuje nějaký způsob, jak rozpoznat, kdy komponenta formátu stránky zpracuje poslední stránku?

Komponenta **Stránka** [nezveřejňuje](er-fillable-excel.md#page-component-limitations) informace o číslu zpracované stránky a celkovém počtu stránek ve vygenerovaném dokumentu. Přesto můžete konfigurovat [vzorce](er-formula-language.md) ER tak, aby rozpoznaly poslední stránku. Následuje příklad:

- Vypočítejte celkový počet transakcí, které již byly zpracovány pomocí komponenty **Stránka sestavy**. Tento výpočet provedete pomocí vzorce `COUNT(Total.Page.Amount.Result)`. 
- Vypočítejte celkový počet transakcí, které musí být zpracovány na základě vazby `model.CommodityRecord`, která je konfigurována pro komponentu **Řádky sestavy**. Tento výpočet provedete pomocí vzorce `COUNT(model.CommodityRecord)`.
- Porovnáním dvou čísel rozpoznáte poslední stránku. Když jsou obě hodnoty stejné, vygeneruje se poslední stránka.

> [!NOTE]
> Tento přístup doporučujeme použít pouze v případě, kdy vlastnost **Povoleno** komponenty **Řádky sestavy** neobsahuje žádný vzorec, který by mohl za běhu sestavy vrátit [False](er-formula-supported-data-types-primitive.md#boolean) pro některé iterované [záznamy](er-formula-supported-data-types-composite.md#record) vázaného [seznamu záznamů](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Další prostředky

- [Návrh konfigurace pro generování dokumentů ve formátu Excel](er-fillable-excel.md)
- [Použití zdrojů dat SHROMAŽĎOVÁNÍ DAT ve formátech elektronického výkaznictví (ER)](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
