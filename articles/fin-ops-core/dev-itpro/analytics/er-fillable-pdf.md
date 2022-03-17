---
title: Návrh konfigurací elektronického výkaznictví pro vyplnění šablon PDF
description: Toto téma obsahuje informace o tom, jak navrhnout formát elektronického výkaznictví pro vyplnění šablony PDF.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: a568ddd93bfbc7d536e951a13470b3dedb796e1b
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367810"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Návrh konfigurací elektronického výkaznictví pro vyplnění šablon PDF

[!include[banner](../includes/banner.md)]

Postupy v tomto tématu jsou příklady, které ukazují, jak může uživatel v roli **správce systému** nebo **vývojáře elektronického výkaznictví** konfigurovat formát elektronického výkaznictví, který generuje sestavy jako soubory PDF použitím vyplnitených PDF dokumentů jako šablon sestav. Tyto kroky lze provádět ve jakékoliv společnosti Dynamics 365 Finance nebo službě Regulatory Configuration Services (RCS).

## <a name="prerequisites"></a>Předpoklady

Než začnete, musíte mít v závislosti na službě, kterou používáte k dokončení postupů v tomto tématu, jeden z následujících typů přístupu:

- Přístup k Finance pro některou z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Přístup k RCS pro některou z následujících rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

Je také nutné dokončit postup [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Nakonec si stáhněte následující soubory.

| Popis obsahu                       | Název souboru                                     |
|-------------------------------------------|-----------------------------------------------|
| Šablona pro první stránku sestavy | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Šablona pro další stránky sestavy    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Ukázkový formát elektronického výkaznictví - PDF                          | [Sestava Intrastat (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Ukázkový formát elektronického výkaznictví - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Ukázková datová sada                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Návrh konfigurace formátu

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft

1. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.
2. Ujistěte se, že je k dispozici zprostředkovatel **Litware, Inc.** a je označen jako aktivní.
3. Na dlaždici pro poskytovatele **Microsoft** vyberte **Úložiště**.

    > [!NOTE]
    > Pokud již existuje úložiště typu **LCS**, přeskočte zbývající kroky tohoto postupu.

4. Vyberte **přidat**.
5. V rozevíracím dialogovém okně ve skupině polí **Typ úložiště konfigurace** vyberte možnost **LCS**.
6. Zvolte **Vytvořit úložiště**.
7. Vyberte **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Získání konfigurací modelů poskytnutých společností Microsoft

1. Na levé straně stránky **Úložiště konfigurací** vyberte tlačítko **Zobrazit filtry** (symbol trychtýře).
2. Přidejte filtr pro hodnotu **LCS** v poli **Typ** a použijte operátor **začíná na**.
3. Zvolte **Použít**.
4. Zvolte **Otevřít**.
5. Ve stromovém zobrazení vyberte **Modul Intrastat**.
6. Na záložce s náhledem **Verze** vyberte verzi **1**.

    > [!NOTE]
    > Pokud není tlačítko **Importovat** na záložce s náhledem **Verze** k dispozici, přeskočte zbývající kroky tohoto postupu.

7. Vyberte **Import**.
8. Vyberte možnost **Ano**, chcete-li potvrdit import vybrané verze konfigurace **Modelu Intrastat**.

### <a name="create-a-new-format-configuration"></a>Vytvoření nové konfigurace formátu

1. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
2. Ve stromovém zobrazení vyberte **Modul Intrastat**.
3. Vyberte **Vytvořit konfiguraci**.

    > [!NOTE]
    > Pokud není tlačítko **Vytvořit konfiguraci** k dispozici, je nutné na stránce **Parametry elektronického výkaznictví** zapnout režim návrhu, který lze otevřít z pracovního prostoru **Elektronické výkaznictví**.

4. V rozevíracím dialogovém okně ve skupině polí **Nový** vyberte možnost **Formát založený na datovém modelu Intrastat**.
5. Do pole **Název** zadejte **Sestava Intrastat (PDF)**.
6. Do pole **Popis** zadejte **Sestava Intrastat ve formátu PDF**.

    > [!NOTE]
    > Aktivní poskytovatel konfigurace se zadá automaticky. Tento zprostředkovatel bude moci udržovat tuto konfiguraci. I když jiní poskytovatelé mohou použít tuto konfiguraci, nebudou ji moci spravovat.

7. Volitelné: V poli **Typ formátu** můžete vybrat konkrétní formát elektronického dokumentu. Pokud vyberete **PDF** v době návrhu, návrhář operací ER nabídne pouze prvky formátu, které jsou použitelné pouze pro dokumenty generované ve formátu PDF (**PDF\File**, **PDF\PDF Merger** atd.). Pokud toto pole ponecháte prázdné, bude v době návrhu určen formát elektronického dokumentu v návrháři operací ER, když je přidán první prvek formátu. Přidáte-li například **Excel\Soubor** jako první prvek formátu, návrhář operací ER vám nabídne pouze prvky formátu, které jsou použitelné pouze pro dokumenty generované ve formátu aplikace Excel (**Excel\Cell,**, **Excel\Range** atd.). formát.
8. Vyberte **Vytvořit konfiguraci**.

Vytvoří se nová konfigurace formátu elektronického výkaznictví. Můžete použít verzi konceptu této konfigurace pro uložení komponenty formátu elektronického výkaznictví, která je určena pro generování elektronických dokumentů ve formátu PDF.

### <a name="design-the-format-of-an-electronic-document"></a>Návrh formátu elektronického dokumentu

Poté ve vytvořené konfiguraci formátu elektronického výkaznictví navrhnete formát elektronického výkaznictví, který generuje sestavu **Kontrola Intrastat** ve formátu PDF. Na první stránce této sestavy musí být uveden souhrn sestavy a podrobnosti o transakcích zahraničního obchodu, které jsou vykazovány. Na dalších stránkách musí být uvedeny pouze podrobnosti o transakcích zahraničního obchodu, které jsou vykazovány. Protože generované stránky sestavy musí mít různá rozvržení, budou ve formátu elektronického výkaznictví použity dvě různé šablony ve formátu PDF.

V libovolném prohlížeči PDF otevřete stažené šablony PDF. Všimněte si, že každá šablona obsahuje více polí, která musí být vyplněna. V každé šabloně jsou podrobnosti o transakcích zahraničního obchodu prezentovány jako 42 řádků, z nichž každý má devět polí. Číslo řádku se zobrazí na konci názvu každého pole (například **Datum 1**...**Datum 42** a **Komodita 1**...**Komodita 42**).

Na následujícím obrázku je zobrazena šablona PDF pro první stránku sestavy.

![Šablona 1.](media/rcs-ger-filloutpdf-template1.png)

Na následujícím obrázku je zobrazena šablona PDF pro další stránky sestavy.

![Šablona 2.](media/rcs-ger-filloutpdf-template2.png)

1. Na stránce **Konfigurace** zvolte **Návrhář**.
2. Vyberte **Přidat kořen**.
3. V rozevíracím dialogovém okně ve stromu vyberte **PDF \> PDF Merger**.

    Když vyberete prvek **PDF Merger** jako kořenový prvek formátu, všechny dokumenty PDF generované za běhu budou sloučeny do jednoho finálního dokumentu PDF. Pokud potřebujete pouze jednu šablonu PDF pro generování všech požadovaných dokumentů pomocí navrženého formátu elektronického výkaznictví, můžete vybrat **Soubor PDF** jako kořenový prvek.

4. Do pole **Název** zadejte **Výstup**.
5. V poli **Jazykové předvolby** vyberte **Uživatelské předvolby**. Sestava bude vygenerována v preferovaném jazyce uživatele, který ji spustil.
6. V poli **Předvolby jazykové verze** vyberte **Uživatelské předvolby**. Hodnoty a data, která jsou uvedena na stránkách sestavy, budou formátována na základě preferovaného národního prostředí uživatele, který sestavu spustí.
7. Vyberte **OK**.
8. V podokně akcí na kartě **Importovat** zvolte **Importovat z PDF**.

    Když je vyplnitelný dokument PDF importován jako šablona pro tento formát elektronického výkaznictví, všechny požadované prvky formátu elektronického výkaznictví (prvky **Soubor PDF**, **Skupina polí** a **Pole**) se automaticky vytvoří ve formátu, který je navržen, na základě struktury importovaného dokumentu PDF.

9. Vyberte **Procházet**. Přejděte k souboru **IntrastatReportTemplate1. PDF**, který jste stáhli dříve jako předpoklad, a vyberte ho.
10. Vyberte **OK**.

    Vybraný soubor se načte a pole **Šablona** v dialogovém okně **Importovat z PDF** se vyplní.

11. Nastavte možnost **Pole skupiny** na **Ano**. Pokud vybraný dokument PDF obsahuje skupiny polí, budou použity k seskupení vytvořených prvků formátu elektronického výkaznictví. Pro tento účel bude vytvořen prvek formátu **Skupina polí**.

    Je-li tato možnost nastavena na hodnotu **Ne**, budou požadované prvky formátu elektronického výkaznictví vytvořeny jako prostý seznam prvků, které jsou vnořeny pod vytvořeným prvkem formátu **Soubor PDF**.

12. Vyberte **OK**.

    ![Dialogové okno Importovat z PDF.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Ve stromu rozbalte **Výstup**.

    Všimněte si, komponenta **Soubor PDF** byla automaticky vytvořena za účelem správy vytvoření první stránky sestavy, která je generována za běhu.

14. Ve stromu rozbalte **Výstup \> Soubor PDF**.

    Všimněte si, že strukturovaný seznam prvků formátu byl automaticky vytvořen v tomto formátu elektronického výkaznictví na základě struktury vyplnitelného dokumentu PDF, který jste importovali dříve.

15. Ve stromu vyberte **Výstup \> Soubor PDF**.
16. Do pole **Název** zadejte **Strana 1**.

    Tento prvek formátu bude použit k vygenerování první stránky sestavy **Kontrola Intrastat**. Na této stránce bude zobrazen souhrn sestavy a podrobnosti o transakcích zahraničního obchodu.

    Pokud ponecháte pole **Jazykové předvolby** prázdné, nastavení **Jazykové předvolby** nadřazeného prvku **PDF Merger** určí jazyk sestavy, která je generována pomocí tohoto prvku formátu. Chcete-li přepsat nastavení nadřazeného prvku, můžete vybrat jinou hodnotu.

    Pokud ponecháte pole **Předvolby jazykové verze** prázdné, nastavení **Předvolby jazykové verze** nadřazeného prvku **PDF Merger** určí národní prostředí sestavy, která je generována pomocí tohoto prvku formátu. Národní prostředí určuje formát hodnot a dat na stránkách sestavy. Chcete-li přepsat nastavení nadřazeného prvku, můžete vybrat jinou hodnotu.

17. V podokně akcí vyberte kartu **Importovat** . Povšimněte si, že bude k dispozici tlačítko **Aktualizovat z PDF** pro zvolený prvek formátu **Soubor PDF**.

    Toto tlačítko slouží k importu aktualizované šablony PDF do upraveného formátu. Po importu aktualizované šablony PDF se odpovídajícím způsobem změní seznam prvků formátu:

    - U všech nových polí v aktualizované šabloně PDF jsou vytvořeny nové prvky formátu v upraveném formátu elektronického výkaznictví.
    - Pokud aktualizovaná šablony PDF již neobsahuje pole, která odpovídají jakýmkoli existujícím prvkům formátu v upraveném formátu elektronického výkaznictví, budou tyto prvky formátu odstraněny z formátu elektronického výkaznictví.

18. Na kartě **Formát** vyberte **Přílohy**.

    Všimněte si, že importovaný dokument PDF je připojen k upravenému formátu elektronického výkaznictví.

    ![Náhled přílohy PDF.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Pokračujte v návrhu tohoto formátu importováním druhé šablony PDF, přidáním potřebných vazeb do datových zdrojů a tak dále.
20. Zvolte **Uložit**.
21. Zavřete stránku.
22. Zvolte **Odstranit**.
23. Vyberte **Ano**.

Chcete-li se dozvědět, jak lze použít nové prvky formátu **PDF Merger**, **Soubor PDF**, **Skupina polí** a **Pole** PDF k vygenerování dokumentů ve formátu PDF, můžete importovat a analyzovat ukázkový formát elektronického výkaznictví.

### <a name="import-the-format-configuration"></a>Importování konfigurace formátu

Poté naimportujete ukázkový formát elektronického výkaznictví, který jste dříve stáhli, za účelem generování sestavy **Kontrola Intrastat** ve formátu PDF. Na první stránce této sestavy musí být uveden souhrn sestavy a podrobnosti o transakcích zahraničního obchodu, které jsou vykazovány. Na dalších stránkách musí být uvedeny pouze podrobnosti o transakcích zahraničního obchodu, které jsou vykazovány.

1. Na stránce **Konfigurace** vyberte **Exchange \> Načíst ze souboru XML**.
2. Vyberte **Procházet**. Přejděte k souboru **Intrastat report (PDF).version.1.1.xml**, který jste stáhli dříve jako předpoklad, a vyberte ho.
3. Vyberte **OK**.

## <a name="analyze-the-format-configuration"></a>Analyzování konfigurace formátu

### <a name="format-layout"></a>Rozvržení formátu

1. Na stránce **Konfigurace** vyberte ve stromu **Modul Intrastat \> Sestava Instrastat (PDF).**
2. Vyberte možnost **Návrhář**.
3. Vyberte **Zobrazit podrobnosti**.
4. Ve stromu rozbalte **Výstup: PDF Merger**.

    Všimněte si, že tento formát elektronického výkaznictví obsahuje dva prvky **Soubor PDF**, z nichž každý používá jinou šablonu PDF. Jedna šablona se používá ke generování první stránky sestavy ve formátu PDF a druhá se použije ke generování dalších stránek.

5. Ve stromové struktuře rozbalte **Výstup: PDF Merger \> Strana 1: Soubor PDF (IntrastatReportTemplate1)**.
6. Ve stromové struktuře rozbalte **Výstup: PDF Merger \> Strana N: Soubor PDF (IntrastatReportTemplate2)**.

    Všimněte si, že protože obsah dvou šablon PDF se liší, struktura vnořených prvků formátu pro dva prvky **Soubor PDF** se také liší.

### <a name="format-mapping"></a>Mapování formátu

1. Na stránce **Návrhář formátu** vyberte kartu **Mapování.**
2. Ve stromu rozbalte **Stránkování \> Strany**.

    ![Stránka návrháře receptury, na které je rozbalen strom modelu.](media/rcs-ger-filloutpdf-reviewformat.png)

    Mějte na paměti následující podrobnosti:

    - Prvek formátu **Výstup \> Strana 1** typu **Soubor PDF** není vázán na žádný zdroj dat a výraz **Povoleno** tohoto prvku formátu je prázdný. Proto v době běhu bude PDF šablona **IntrastatReportTemplate1** vyplněna pouze jednou při vygenerování jednotlivého dokumentu PDF.
    - Prvek formátu **Výstup \> Strana N** typu **Soubor PDF** je vázán na datový zdroj **Paging.PageN** typu **Seznam záznamů** a výraz **Povoleno** tohoto prvku formátu je prázdný. Proto v době běhu bude PDF šablona **IntrastatReportTemplate2** vyplněna pro každý záznam z vázaného seznamu záznamů při vygenerování jednotlivého dokumentu PDF.
    - Protože prvky formátu **Strana 1: Soubor PDF** a **Strana N: Soubor PDF** jsou podřízenými prvky prvku formátu **Výstup: PDF Merger** všechny dokumenty PDF, které jsou vyplněny, budou sloučeny do jediného finálního dokumentu PDF.
    - Zdroje dat **Paging.Page1** a **Paging.PageN** jsou nakonfigurovány jako filtry záznamů z datového zdroje **Paging.Pages**. Tento zdroj dat je nakonfigurován tak, aby rozdělil celou sadu transakcí zahraničního obchodu do dávek. Každá dávka obsahuje až 42 záznamů. Následující výraz elektronického výkaznictví se používá k rozdělení transakcí do dávek:

        SPLITLIST(Totals.CommodityRecord,42)

    - Datový zdroj **Paging.Pages** obsahuje prvek **Paging.Pages.Enumerated**, který vrací podrobné informace o každém záznamu, který je obsažen v dávce. Tyto podrobnosti zahrnují pořadí záznamu v aktuální dávce (pole **Paging.Pages.Enumerated.Number**). Pole **Paging.Pages.Enumerated.Number** se používá ve výrazu **Název** prvků formátu **Pole PDF** s cílem dynamického generování názvu pole, které je založeno na čísle transakce v dávce. Vygenerovaný název pole se pak používá k vyplnění správného pole PDF v použité šabloně PDF.
    - Prvek formátu **Výstup \> Strana N \> Podrobnosti 2** typu **Skupina PDF** je vázán na zdroj dat **Paging.PageN.Enumerated** (nebo **\@.Enumerated**, pokud se používá režim zobrazení **Relativní cesta**) typu **Seznam záznamů**. Za běhu tedy budou pro každý záznam z vázaného seznamu záznamů vyplněny vnořené prvky této skupiny PDF. Tímto způsobem jsou jednotlivé řádky PDF virtuálně generovány, když pro každý n-tý ze 42 záznamů seznamu **Paging.PageN.Enumerated** jsou vyplněna následující pole PDF: datum N, Směr N, Komodita N, atd. Proto v tomto ohledu chování tohoto prvku formátu **Skupina polí** připomíná chování prvků formátu **XML \> Pořadí** a **Text \> Pořadí**.

3. Ve stromové struktuře rozbalte **Výstup \> Strana N \> Podrobnosti2**.
4. Ve stromové struktuře vyberte **Výstup \> Strana N \> Podrobnosti 2 \> PageFooter**.

    Všimněte si, že atribut **Název** tohoto prvku formátu je definován jako **PageFooter**. Všimněte si také, že výraz **Název** prvku formátu je prázdný.

5. Ve stromové struktuře vyberte **Výstup \> Strana N \> Podrobnosti 2 \> Oprava 1**.

    Všimněte si, že atribut **Název** tohoto prvku formátu je definován jako **Oprava 1**. Všimněte si také, že výraz **Název** prvku formátu je definován jako **Paging.FldName("Oprava",\@.Number)**.

![Návrhář formátu, kde je vybráno mapování.](media/rcs-ger-filloutpdf-reviewformat2.png)

Všimněte si, že prvek formátu **Pole** se používá k vyplnění jednotlivého pole vyplnitelného dokumentu PDF, který je definován jako šablona nadřazeného prvku formátu **Soubor PDF**. Vazba prvku formátu **Soubor PDF** nebo jeho vnořených prvků, pokud obsahuje vnořené prvky, určuje hodnotu, která je zadána do odpovídajících polí PDF. Různé vlastnosti prvku formátu **Pole** lze použít k určení toho, které pole PDF je vyplněno pomocí jednotlivého prvku formátu:

- Na kartě **Formát** se jedná o atribut **Název** prvku formátu
- Na kartě **Mapování** se jedná o výraz **Název** prvku formátu

Vzhledem k tomu, že obě vlastnosti jsou pro prvek formátu **Pole** volitelné, jsou pro určení cílového pole PDF použita následující pravidla:

- Pokud je atribut **Název** prázdný a výraz **Název** vrací prázdný řetězec za běhu, je vyvolána výjimka za běhu, která upozorní uživatele, že pole PDF nelze nalézt v šabloně PDF, která se používá k vyplnění PDF dokumentu.
- Je-li atribut **Název** definován a výraz **Název** je prázdný, bude vyplněno pole PDF, které má stejný název jako atribut **Název** prvku formátu.
- Je-li atribut **Název** definován a výraz **Název** je nakonfigurovaný, bude vyplněno pole PDF, které má stejný název jako hodnota vrácená výrazem **Název** prvku formátu.

> [!NOTE]
> Zaškrtávací políčko PDF lze vyplnit tak, jak bylo vybráno následujícími způsoby:
>
> - Když je odpovídající prvek formátu **Pole** svázán s polem zdroje dat typu **Logický**, který má hodnotu **True**
> - Pokud odpovídající prvek formátu **Pole** obsahuje vnořený prvek formátu **Řetězec**, který je svázán s polem zdroje dat, které má textovou hodnotu **1**, **True** nebo **Ano**.

## <a name="run-the-format-configuration"></a>Spuštění konfigurace formátu

### <a name="import-the-format-configuration"></a>Importování konfigurace formátu

Dále načtete vzorový formát elektronického výkaznictví **Intrastat (import z aplikace Excel)**. Tento formát je určen k analýze uživatelem vybraného sešitu Microsoft Excel, který simuluje transakce zahraničního obchodu.

1. Na stránce **Konfigurace** vyberte **Exchange \> Načíst ze souboru XML**.
2. Vyberte **Procházet**. Přejděte k souboru **Intrastat (import z aplikace Excel).version.1.1.xml**, který jste stáhli dříve jako předpoklad, a vyberte ho.
3. Vyberte **OK**.
4. Ve stromové struktuře vyberte **Modul Intrastat \> Intrastat (import z aplikace Excel)**.
5. Vyberte možnost **Upravit**.
6. Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.

    > [!NOTE]
    > Pokud jste dříve nastavili možnost **Výchozí pro mapování modelu jiné** na **Ano** pro konfiguraci **modulu Intrastat** nebo jinou konfiguraci, která je vnořená pod konfigurací **modulu Intrastat**, nastavte tuto možnost na **Ne**.

    Je-li možnost **Výchozí pro mapování modelu** nastavena na **Ano**, bude formát elektronického výkaznictví **Intrastat (import z aplikace Excel)** přiřazen jako výchozí zdroj dat pro konfiguraci formátu **sestavy Intrastat (PDF)**. Poté, co je spuštěna konfigurace formátu **sestavy Intrastat (PDF),** bude obsah sešitu aplikace Excel, který je analyzovaný formátem elektronického výkaznictví **Intrastat (import z aplikace Excel)**, simulovat transakce zahraničního obchodu, které musí být vykázány. Následující obrázek znázorňuje příklad sešitu aplikace Excel.

    ![Sešit aplikace Excel, který obsahuje ukázková data.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Spuštění konfigurace formátu

1. Na stránce **Konfigurace** vyberte ve stromu **Modul Intrastat \> Sestava Instrastat (PDF).**
2. Vyberte **Spustit**.
3. Vyberte **Procházet**. Přejděte k souboru **Intrastat sample data.xlsx**, který jste stáhli dříve jako předpoklad, a vyberte ho.
4. Vyberte **OK**.
5. V poli **Směr sestavy** zvolte **Obojí** pro vyplnění všech transakcí z importovaného sešitu aplikace Excel v sestavě PDF, která je vygenerována.
6. Vyberte **OK**.
7. Zkontrolujte vygenerovaný dokument PDF.

Následující obrázek znázorňuje příklad první stránky vygenerované sestavy.

![První stránka vygenerované sestavy.](media/rcs-ger-filloutpdf-generatedreport.png)

Následující obrázek znázorňuje příklad další stránky vygenerované sestavy.

![Další stránka vygenerované sestavy.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Omezení

Názvy vyplnitelných polí by měly být jedinečné ve formuláři PDF, který chcete použít jako šablonu zprávy. Pro každé takové pole je při importu formuláře PDF vytvořen samostatný prvek formátu s odpovídajícím názvem v upravitelném formátu ER. Pokud formulář PDF obsahuje několik polí se stejným názvem, vytvoří se pro pole jeden prvek formátu, který neumožňuje jednotlivá vyplnění za běhu.

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>Když spustím formát ER pro generování zprávy ve formátu PDF, proč se mi zobrazují následující chyby: **Nelze zpracovat iref streamy. Současná implementace PDFSharp nezvládá tuto funkci PDF zavedenou s Acrobatem 6.** a **Název PDF musí začínat lomítkem (/).**

Rámec ER používá ke generování těchto zpráv PDF verzi 1.5 knihovny PDFSharp. Některé funkce PDF 1.5 (Adobe Reader 6.0) ještě nejsou v této knihovně implementovány. Proto PDFSharp zatím nemůže otevřít některé soubory, které jsou označeny jako **pro PDF 1.5 nebo vyšší** a může mít za následek obdržené chyby. K vyřešení problému použijte jedno z následujících řešení:

-   Když používáte vlastní šablonu PDF: Přejděte na nižší verzi šablony Adobe a začněte používat novou šablonu ve vašem formátu ER.
-   Když používáte šablonu formátu ER, kterou s vámi sdílel jiný poskytovatel konfigurace jako součást řešení ER: Kontaktujte vlastníka tohoto řešení ER a poskytněte mu popis problému.
-   Když používáte řešení ISV, které obsahuje dřívější verzi knihovny PDFSharp: Kontaktujte vlastníka řešení a navrhněte mu upgrade na novější verzi PDFSharp.

## <a name="additional-resources"></a>Další prostředky

- [Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML (listopad 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
