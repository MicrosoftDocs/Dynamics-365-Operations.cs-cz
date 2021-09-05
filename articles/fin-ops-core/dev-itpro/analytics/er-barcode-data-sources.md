---
title: Ke generování obrázků čárových kódů použijte zdroje dat čárového kódu
description: Toto téma vysvětluje, jak používat zdroje dat čárového kódu pro generování obrázků čárových kódů.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 72c79c37ca5b5f98637ba5069e25465bb1391306
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343256"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Ke generování obrázků čárových kódů použijte zdroje dat čárového kódu

[!include[banner](../includes/banner.md)]

Můžete použít rámec [Elektronické hlášení (ER)](general-electronic-reporting.md) pro návrh [Komponent formátu ER](general-electronic-reporting.md#FormatComponentOutbound), které můžete spustit a generovat tak elektronické a tisknutelné odchozí dokumenty, které potřebujete. Chcete-li vygenerovat odchozí dokument ve formátu Microsoft Office, musíte určit rozložení sestavy pomocí dokumentu Microsoft Excel nebo Microsoft Word jako šablonu sestavy. [Návrhář operací ER](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) umožňuje připojit dokument Excel nebo Word jako šablonu pro formát ER. Následující pojmenované prvky v připojené šabloně jsou spojeny s prvky konfigurované komponenty formátu:

- Ovládací prvky obsahu v aplikaci Word
- Pojmenované listy, rozsahy, buňky, tvary a obrázky v Excelu

Tyto pojmenované prvky se používají jako zástupné symboly pro data, která se zadávají do generovaného dokumentu při spuštění formátu ER. Prvky formátu ER jsou vázány na zdroje dat. Tyto zdroje dat určují data, která budou za běhu zadána do vygenerovaných dokumentů. Další informace viz [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).

ER nyní podporuje typ zdroje dat **čárový kód**. Proto nyní můžete vygenerovat obrázek, který představuje čárový kód pro zadaný text. Když konfigurujete formát ER, můžete určit zdroje dat typu **čárového kódu** pro generování obrázků čárového kódu. Tyto obrázky pak můžete přidat do generovaných obchodních dokumentů, jako jsou objednávky, faktury, dodací listy a účtenky. Můžete je také přidat k různým druhům štítků, jako jsou štítky produktů a polic a štítky obalů a zásilek.

Následující zástupné symboly lze použít v šablonách sestav pro zadávání obrázků čárových kódů:

- [Obrázek](/office/client-developer/word/content-controls-in-word) řízení obsahu pro Word
- [Obrázek](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) objekt v Excelu

Použitím zdroje dat typu **čárový kód** můžete generovat čárové kódy v následujících formátech:

- Jednorozměrné čárové kódy:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Inteligentní pošta
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Dvojrozměrné čárové kódy:

    - Aztec
    - Datová matice
    - QR kód

Při konfiguraci zdroje dat **čárového kódu** můžete definovat specifické parametry vykreslování, které se používají ke generování obrazu:

- **Šířka** - Určete šířku čárového kódu v pixelech. Hodnota **0** (nula) označuje, že je použita výchozí šířka. Význam se může u různých formátů lišit.
- **Výška** - Určete výšku čárového kódu v pixelech. Hodnota **0** (nula) označuje, že je použita výchozí výška. Význam se může u různých formátů lišit.
- **Okraj** - Určete velikost okraje čárového kódu v pixelech. Okraj je oblast na každé straně čárového kódu, která musí být udržována v čistotě (tichá zóna). Hodnota **0** (nula) označuje, že je použita výchozí velikost okraje. Význam se může u různých formátů lišit.
- **Výstupní obsah** - Nastavte hodnotu na **Ano** pro generování obrazu čárového kódu, který obsahuje kódované informace jako text. Výchozí hodnota je **Ne**.
- **Kódování** - Určete typ znaků, které jsou kódovány ve vygenerovaném obrázku čárového kódu. Ve výchozím nastavení je použito kódování **UTF-8**.

> [!IMPORTANT]
> Když přidáte nový zdroj dat **čárového kódu**, musíte jej umístit pod jinou položku (kontejner) jako vnořený prvek.
>
> Když vážete zdroj dat **čárový kód** do buněčného prvku ve formátu a buněčný prvek představuje buď ovládací prvek obsahu Word nebo obrázek Excel, zdroj dat je prezentován v této vazbě jako funkce, která má jediný parametr typu **Řetězec**. Tento parametr musíte použít k určení textu, který by měl být převeden na obrázek čárového kódu, a číst při skenování vygenerovaného čárového kódu.

Chcete-li získat další informace o této funkci, proveďte příklady tomto tématu.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Příklad: Vygenerujte platební šek, který obsahuje čárový kód, který kóduje splatnou částku

Tento příklad ukazuje, jak uživatel s rolí **Správce systému** nebo **Funkční poradce pro elektronický reporting** může konfigurovat formát ER, který obsahuje šablonu, která se používá ke generování odchozího dokumentu ve formátu Excel, který obsahuje čárový kód. Zde je přehled kroků, které jsou zahrnuty.

1. [Vyplňte předpoklady](#ExamplePrerequisites).
2. [Aktivace poskytovatele konfigurace](#ExampleProvider).
3. [Importovat poskytnuté řešení ER](#ExampleImportSolution).
4. [Vygenerování platebního šeku](#ExampleGenerateCheque).
5. [Kontrola generovaného platebního šeku](#ExampleReviewGeneratedCheque).
6. [Upravte formát poskytovaného řešení ER](#ExampleModifyFormat).

    1. [Použijte novou šekovou šablonu](#ExampleModifyFormatApplyTemplate).
    2. [Přidání nového zdroje čárového kódu](#ExampleModifyFormatAddDataSource).
    3. [Vázat nový prvek formátu](#ExampleModifyFormatBindFormatElement).
    4. [Zpřístupněte upravenou verzi pro zkušební spuštění](#ExampleModifyFormatMakeVersionAvailable).

        1. [Dokončete verzi upraveného formátu](#CompleteToRun).
        2. [Zpřístupněte verzi konceptu k použití](#MarkToRun).

7. [Vygenerování platebního šeku](#ExampleGenerateCheque2).
8. [Převést vygenerovaný šek na PDF](#ExampleConvertToPDF).

V tomto příkladu použijete poskytované řešení ER, které bylo nakonfigurováno pro generování platebních šeků. Toto řešení generuje platební šeky, kde je splatná částka zapsána jako číslo i jako text. Toto řešení ER upravíte tak, aby šek obsahoval také vygenerovaný čárový kód, ve kterém je kódována splatná částka a lze ji přečíst pomocí skeneru čárových kódů.

Tyto kroky lze dokončit ve společnosti **USMF** v aplikaci Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Vyplňte předpoklady

K dokončení tohoto příkladu v tomto tématu musíte mít přístup ke společnosti USMF v aplikaci Finance pro některou z následujících rolí:

- Funkční konzultant elektronického výkaznictví
- Správce systému

Pokud jste ještě nedokončili příklad v části [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md), stáhněte si následující konfigurace ukázkového řešení elektronického výkaznictví.

| Popis obsahu         | Název souboru                   |
|-----------------------------|-----------------------------|
| Konfigurace datového modelu elektronického výkaznictví | [Model pro cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)      |
| Konfigurace formátu elektronického výkaznictví     | [format.xml pro tisk šeků](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |

Dále si stáhněte následující soubor Excel, který obsahuje upravenou šablonu pro poskytnuté řešení ER.

| Popis obsahu | Název souboru                 |
|---------------------|---------------------------|
| Šablona sestavy     | [Zkontrolujte šablonu Excel.xlsx](https://download.microsoft.com/download/3/b/d/3bd3b944-da8f-43b4-8533-3c1292a4c3ef/CheckTemplateExcel.xlsx) |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Aktivace poskytovatele konfigurace

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurace** ověřte, že je uveden [poskytovatel konfigurace](general-electronic-reporting.md#Provider) ukázkové společnosti **Litware, Inc.** a že je označen jako aktivní. Není-li uveden v seznamu nebo není-li označen jako aktivní, postupujte podle kroků v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Nastavení ukázkové společnosti Litware, Inc. do aktivního stavu na stránce konfigurace lokalizace.](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Importovat poskytnuté řešení ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace**, pokud konfigurace **Model pro šeky** není ve stromu konfigurací k dispozici, pomocí následujících kroků importujte konfiguraci datového modelu elektronického výkaznictví:

    1. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
    2. V dialogovém okně vyberte **Procházet** najděte a vyberte soubor **Model for cheques.xml** a poté vyberte **OK**.

4. Pokud konfigurace **Formát pro tisk šeků** není ve stromu konfigurací k dispozici, pomocí následujících kroků importujte konfiguraci formátu elektronického výkaznictví:

    1. V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.
    2. V dialogovém okně vyberte **Procházet** najděte a vyberte soubor **Cheques printing format.xml** a poté vyberte **OK**.

5. Ve stromu konfigurace rozbalte **Model pro šeky**.
6. Zkontrolujte seznam importovaných konfigurací elektronického výkaznictví ve stromu konfigurace.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Vygenerování platebního šeku

1. Přejděte do části **Pokladna a banka** \> **Bankovní účty** \> **Bankovní účty**.
2. Na stránce **Bankovní účty** vyberte účet **USMF OPER**.
3. Na stránce s podrobnostmi o bankovním účtu v podokně akcí na kartě **Nastavení** ve skupině **Rozložení** vyberte **Kontrola**.
4. Na stránce **Kontrola rozložení** vyberte **Upravit**.
5. Na pevné záložce **Obecné** nastavte volbu **Obecný formát elektronického exportu** na **Ano**.
6. V poli **Exportovat konfiguraci formátu** vyberte formát elektronického výkaznictví **Formát tisku šeků**, který jste dříve importovali.
7. V podokně akcí klikněte na možnost **Test tisku**.
8. V dialogovém okně nastavte **Dohodnutelný formát kontroly** na **Ano** a poté vyberte **OK**.

    ![Zkontrolujte rozložení – dialogové okno testu tisku.](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Kontrola generovaného platebního šeku

- Otevřete vygenerovaný šek v Excelu.
2. Prohlédněte si vygenerovaný šek.

    ![Vygenerovaný platební šek v Excelu.](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Upravte formát poskytovaného řešení ER

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Použijte novou šekovou šablonu

Aplikací na ploše Excel můžete otevřít soubor **Cheque template Excel.xlsx**, který jste importovali dříve. Všimněte si, že se tato šablona liší od šablony, kterou jste použili ke generování platebního šeku v dodávaném řešení ER. Kromě toho obsahuje prvek **AmountBarcode** pro obrázek čárového kódu.

![Prvek AmountBarcode v šabloně Excel.](./media/er-barcode-data-source-cheque2.png)

Nyní musíte upravit řešení ER a poté [znovu použít](modify-electronic-reporting-format-reapply-excel-template.md) upravenou šablonu.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurace rozbalte **Model pro šeky** a vyberte **Formát tisku šeků**.
4. V podokně akcí zvolte **Návrhář**.
5. V návrháři operací ER vyberte kartu **Mapování** na pravé straně stránky a poté v podokně stromu formátu vlevo vyberte **Rozbalit / sbalit**.
6. Všimněte si, že všechny prvky formátu buňky jsou vázány na příslušné zdroje dat.

    ![Vazba prvků buněčného formátu na zdroje dat v návrháři operací ER.](./media/er-barcode-data-source-cells-bound.png)

7. Vyberte kartu **Formát** na pravé straně stránky.
8. V podokně akcí vyberte tři tečky (**...**) a poté vyberte **Import**.
9. Ve skupině **Import** vyberte **Aktualizace z Excelu** a poté vyberte **Aktualizovat šablonu**.
10. V dialogovém okně přejděte na soubor **Cheque template Excel.xlsx** uložený v počítači, vyberte jej a poté vyberte **OK** k potvrzení, že by se měla vybraná šablona použít.
11. Vyberte kartu **Mapování** na pravé straně stránky a poté v podokně stromu formátu vlevo vyberte **Rozbalit / sbalit**.
12. Všimněte si, že prvek buňky **AmountBarcode** byl přidán do formátu. Tento prvek je spojen s prvkem **AmountBarcode**, který byl přidán do upravené šablony Excel jako zástupný symbol pro obrázek čárového kódu.

    ![Prvek buňky AmountBarcode přidaný do formátu v návrháři operací ER.](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Přidání nového zdroje čárového kódu

Dále musíte přidat nový zdroj dat typu **Čárový kód**.

1. V návrháři operací ER na kartě **Mapování** na pravé straně stránky vyberte zdroj dat **tisk**.
2. Vyberte **Přidat** a pak ve skupině **Funkce** vyberte typ zdroje dat **čárový kód**.

    ![Výběr typu zdroje dat čárového kódu.](./media/er-barcode-data-source-add.png)

3. V dialogovém okně do pole **Název** zadejte **čárový kód**.
4. Ve **Formátu čárového kódu** vyberte **Code 128**.
5. Do pole **Šířka** zadejte **500**.
6. Vyberte **OK**.

    ![Dialogové okno Vlastnosti zdroje dat.](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Vázat nový prvek formátu

Dále musíte nový prvek formátu svázat se zdrojem dat, který jste právě přidali.

1. V návrháři operací ER na kartě **Mapování** na pravé straně stránky vyberte zdroj dat **print\\barcode**.
2. V podokně stromu formátu vlevo vyberte prvek buňky **AmountBarcode** a poté vyberte **Svázat**.
3. V podokně akcí zvolte **Zobrazit podrobnosti**.
4. Všimněte si, že protože zdroj dat **čárový kód** je ve vazbě reprezentován jako funkce, která obsahuje jeden parametr, název prvku vázaného formátu byl automaticky považován za argument tohoto parametru.

    ![Podrobnosti o zdroji čárových kódů v návrháři operací ER.](./media/er-barcode-data-source-bind1.png)

5. Vyberte **Upravit vzorec** a upravte vazbu.

    Nechcete, aby se vrátil název prvku buňky. Proto musíte nakonfigurovat výraz, který vrací text, který obsahuje splatnou částku aktuální kontroly. Protože nadřazený rozsah **ChequeLines** je vázán na zdroj dat **model.cheques**, splatná částka aktuálního šeku je k dispozici v poli **model.cheques.attributes.amount** zdroje dat **Reálný**.

6. V poli **Vzorec** zadejte **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Vyberte **Uložit** a potom zavřete [Návrhář operací ER](general-electronic-reporting-formula-designer.md).
8. Všimněte si, že vazba byla upravena.

    ![Upravená vazba v návrháři operací ER.](./media/er-barcode-data-source-bind2.png)

9. Vyberte **Uložit** a zavřete Návrhář operací ER.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Zpřístupněte upravenou verzi pro zkušební spuštění

Ve výchozím nastavení se používají pouze verze, které mají stav **Dokončeno** a **Sdíleno**, když spustíte formát ER.

Pokud jste dokončili své změny, můžete dokončit svou práci s aktuální verzí pracovní verze a zpřístupnit změny pro použití. Pokyny viz část [Dokončete verzi upraveného formátu](#CompleteToRun), která následuje.

Pokud chcete pokračovat v práci s aktuální verzí konceptu, ale musíte ji použít ke generování šeků, musíte explicitně určit, že chcete použít verzi konceptu formátu pro provedení. Pokyny viz [Zpřístupněte verzi konceptu k použití](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Dokončete verzi upraveného formátu

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurace rozbalte **Model pro šeky** a vyberte **Formát tisku šeků**.
4. Na pevné záložce **Verze** vyberte záznam se stavem **Koncept**.
5. Vyberte **Změnit stav** a poté vyberte **Dokončit**.
6. V dialogovém okně vyberte **OK**.

Stav aktuální verze se změní z **Koncept** na **Dokončeno** a vytvoří se nová verze, která má stav **Koncept**. Pomocí této nové pracovní verze můžete použít další změny.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Zpřístupněte verzi konceptu k použití

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
4. V dialogovém okně nastavte **Spustit nastavení** na **Ano** a poté vyberte **OK**.
5. Ve stromu konfigurace rozbalte **Model pro šeky** a vyberte **Formát tisku šeků**.
6. Nastavte možnost **Spustit koncept** na **Ano**.
7. Zvolte **Uložit**.

Koncept verze vybraného formátu je označen jako dostupný pro použití při spuštění vybraného formátu.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Vygenerování platebního šeku

1. Přejděte do části **Pokladna a banka** \> **Bankovní účty** \> **Bankovní účty**.
2. Na stránce **Bankovní účty** vyberte účet **USMF OPER**.
3. Na stránce s podrobnostmi o bankovním účtu v podokně akcí na kartě **Nastavení** ve skupině **Rozložení** vyberte **Kontrola**.
4. Na stránce **Zkontrolujte rozložení** v podokně Akce vyberte **Test tisku**.
5. V dialogovém okně nastavte **Dohodnutelný formát kontroly** na **Ano**.
6. Vyberte **OK**.
7. Prohlédněte si vygenerovaný šek. Všimněte si, že byl vygenerován čárový kód pro kódování splatné částky šeku.

    ![Generovaný platební šek s čárovým kódem v Excelu.](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Výjimka je vyvolána, pokud argument zdroje dat **čárový kód** nesplňuje příslušné požadavky, které jsou specifické pro formát čárového kódu. Například, když zdroj dat **čárový kód** je volán pro generování čárového kódu [EAN-8](https://wikipedia.org/wiki/EAN-8) pro poskytnutý text, vyvolá se výjimka, pokud délka textu přesáhne sedm znaků.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Převést vygenerovaný šek na PDF

Jak je popsáno v [Vytvářejte tisknutelné formuláře FTI](er-generate-printable-fti-forms.md#finland), můžete pomocí speciálního písma vytvořit čárové kódy v generovaném dokumentu. V tomto případě mohou další transformace generovaného dokumentu záviset na dostupnosti tohoto písma v transformačním prostředí. Pokud se například pokusíte převést dokument do formátu PDF nebo jej zobrazit v prostředí, kde písmo chybí, nebudou čárové kódy vykresleny správně.

Nicméně, když používáte zdroj dat **čárový kód** dat pro výrobu čárových kódů, vykreslování těchto čárových kódů nezávisí na žádném písmu. Proto můžete snadno převádět dokumenty, které obsahují čárové kódy, do formátu PDF. Následující obrázek ukazuje náhled vygenerovaného platebního šeku, který byl [převedený](electronic-reporting-destinations.md#OutputConversionToPDF) do PDF na základě nastavení nakonfigurované ER [destinace](electronic-reporting-destinations.md).

![Náhled PDF platebního šeku.](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Omezení

> [!NOTE]
> Některé generované čárové kódy mají pevný poměr stran. Toto chování má smysl, pokud jste zapnuli funkci **Povolit použití knihovny EPPlus v rámci elektronického výkaznictví** pro práci s dokumenty Excel v ER. V takovém případě je obraz vložen do zástupného symbolu, který má uzamčený poměr stran. Proto, když rozměry zástupného symbolu v šabloně odpovídají poměru obrazu, který je zadán, skutečný obrázek ve vygenerovaném dokumentu by mohl být změněn, aby se zachoval požadovaný poměr stran. Chcete-li zabránit změně velikosti obrázku, použijte zástupný symbol, který má očekávaný poměr stran.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
- [Funkce NUMBERFORMAT](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
