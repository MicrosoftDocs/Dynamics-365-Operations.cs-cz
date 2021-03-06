---
title: Návrh konfigurace pro generování dokumentů ve formátu Excel
description: Toto téma popisuje, jak navrhnout formát elektronického výkaznictví tak, aby vyplnil šablonu Excel, a poté vygenerovat odchozí dokumenty ve formátu Excel.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893901"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Návrh konfigurace pro generování dokumentů ve formátu Excel

[!include[banner](../includes/banner.md)]

Můžete navrhnout konfiguraci formátu [elektronického výkaznictví](general-electronic-reporting.md), která má [součást formátu](general-electronic-reporting.md#FormatComponentOutbound) elektronického výkaznictví, kterou můžete nakonfigurovat tak, aby generovala odchozí dokument ve formátu Microsoft Excel. K tomuto účelu musí být použity specifické komponenty formátu elektronického výkaznictví.

Chcete-li se o této funkci dozvědět více, postupujte podle kroků v tématu [Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Přidání nového formátu elektronického výkaznictví

Při přidání nové konfigurace formátu elektronického výkaznictví pro generování odchozího dokument ve formátu sešitu Excel musíte vybrat hodnotu **Excel** pro atribut formátu **Typ formátu** nebo ponechat atribut **Typ formátu** prázdný.

- Pokud vyberete **Excel**, můžete nakonfigurovat formát tak, aby generoval odchozí dokument pouze ve formátu Excel.
- Pokud atribut necháte prázdný, můžete nakonfigurovat formát tak, aby generoval odchozí dokument v libovolném formátu, který je podporován rámcem elektronického výkaznictví.

Chcete-li nakonfigurovat komponentu formátu elektronického výkaznictví, vyberte v podokně akcí možnost **Návrhář** a otevřete komponentu formátu elektronického výkaznictví pro úpravy v návrháři operací elektronického výkaznictví.

![Stránka Konfigurace](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Součást souboru Excel

### <a name="manual-entry"></a>Ruční zadání

Musíte přidat komponentu **Excel\\Soubor** do nakonfigurovaného formátu elektronického výkaznictví pro generování odchozího dokumentu ve formátu Excel.

![Součást Excel\Soubor](./media/er-excel-format-add-file-component.png)

Chcete-li určit rozvržení odchozího dokumentu, připojte sešit aplikace Excel, který má příponu .xlsx k součásti **Excel\\Soubor**, jako šablonu pro odchozí dokumenty.

> [!NOTE]
> Když ručně připojíte šablonu, musíte použít [typ dokumentu](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), který byl za tímto účelem nakonfigurován v [parametrech elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Přidání přílohy ke komponentě Excel\Soubor](./media/er-excel-format-add-file-component2.png)

Chcete-li určit, jak bude připojená šablona vyplněna při spuštění konfigurovaného formátu elektronického výkaznictví, musíte přidat vnořené komponenty **List**, **Rozsah** a **Buňka** k součásti **Excel\\Soubor**. Každá vnořená součást musí být přidružena l položce s názvem Excel.

### <a name="template-import"></a>Import šablony

Můžete vybrat možnost **Importovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat novou šablonu do prázdného formátu elektronického výkaznictví. V tomto příkladu bude součást **Excel\\Soubor** vytvořena automaticky a k ní bude připojena importovaná šablona. Všechny požadované komponenty elektronického výkaznictví budou také vytvořeny automaticky na základě nalezených položek s názvem Excel.

![Volba možnosti Importovat z Excelu](./media/er-excel-format-import-template.png)

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.

## <a name="sheet-component"></a>Komponenta listu

Komponenta **List** označuje pracovní list přiloženého sešitu aplikace Excel, který musí být vyplněn. Název listu v šabloně Excel je definován ve vlastnosti **List** této komponenty.

> [!NOTE]
> Tato součást je volitelná pro sešity aplikace Excel, které obsahují jeden list.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **List** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vložen příslušný list.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, vygenerovaný dokument nebude obsahovat pracovní list.

![Příklad součásti listu](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Součást rozsahu

Součást **Rozsah** označuje rozsah Excelu, který musí být ovládán touto součástí elektronického výkaznictví. Název rozsahu je definován ve vlastnosti **Rozsah aplikace Excel** této komponenty.

Vlastnost **Směr replikace** určuje, zda a jak bude rozsah opakován v generovaném dokumentu:

- Pokud je vlastnost **Směr replikace** nastavena na **Žádná replikace**, příslušný rozsah aplikace Excel nebude ve vygenerovaném dokumentu opakován.
- Pokud je vlastnost **Směr replikace** nastavena na **Vertikální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován. Každý replikovaný rozsah je umístěn pod původní rozsah v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.
- Pokud je vlastnost **Směr replikace** nastavena na **Horizontální**, příslušný rozsah aplikace Excel bude ve vygenerovaném dokumentu opakován. Každý replikovaný rozsah je umístěn napravo od původního rozsahu v šabloně Excel. Počet opakování je definován počtem záznamů ve zdroji dat typu **Seznam záznamů**, který je vázán na tuto součást elektronického výkaznictví.

Chcete-li se dozvědět více o horizontální replikaci, postupujte podle kroků v části [Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md).

Součást **Rozsah** může mít další vnořené součásti elektronického výkaznictví, které se používají k zadávání hodnot do příslušných pojmenovaných rozsahů aplikace Excel.

- Pokud je některá součást skupiny **Text** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako textová hodnota.

    > [!NOTE]
    > Tento vzor použijte k formátování zadaných hodnot na základě národního prostředí, které je definováno v aplikaci.

- Pokud je součást **Buňka** skupiny **Excel** použita k zadávání hodnot, hodnota se zadává v rozsahu Excelu jako hodnota datového typu, který je definován vazbou součásti **Buňka** (například **Řetězec**, **Skutečný**, nebo **Celé číslo**).

    > [!NOTE]
    > Tento vzor použijte k povolení aplikace Excel pro formátování zadané hodnoty na základě národního prostředí místního počítače, které otevírá odchozí dokument.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Rozsah** k určení, zda musí být komponenta vložena do vygenerovaného dokumentu:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah nepředstavuje celé řádky nebo sloupce, nebude do vygenerovaného dokumentu vyplněn příslušný rozsah.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu a pokud tento rozsah představuje celé řádky nebo sloupce, vygenerovaný dokument bude obsahovat tyto řádky a sloupce jako skryté.

## <a name="cell-component"></a>Součást buňky

Součást **Buňka** se používá k vyplnění pojmenovaných buněk, tvarů a obrázků Excelu. Chcete-li označit objekt pojmenovaný Excel, který musí být vyplněn součástí elektronické výkaznictví **Buňka**, musíte zadat název tohoto objektu ve vlastnosti **Rozsah aplikace Excel** součásti **Buňka**.

Na kartě **Mapování** návrháře operací elektronického výkaznictví můžete nakonfigurovat vlastnost **Povoleno** pro součást **Buňka** k určení, zda ve vygenerovaném dokumentu musí být vyplněn objekt:

- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **True** za běhu, nebo pokud není vůbec nakonfigurován žádný výraz, bude do vygenerovaného dokumentu vyplněn příslušný objekt. Vazba této součásti **Buňka** určuje hodnotu vloženou do příslušného objektu.
- Pokud je výraz vlastnosti **Povoleno** nakonfigurován pro vrácení hodnoty **False** za běhu, příslušný objekt nebude vyplněn ve vygenerovaném dokumentu.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do buňky, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**). V tomto případě je hodnota zadána do buňky jako hodnota stejného typu dat.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do tvaru Excel, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu (například **Řetězec**, **Skutečný**, nebo **Celé číslo**). V tomto případě je hodnota zadána do tvaru Excel jako text tohoto tvaru. Pro hodnoty typů dat, které nejsou **řetězcem**, převod na text se provádí automaticky.

> [!NOTE]
> Můžete nakonfigurovat součást **Buňka** pro vyplnění tvaru pouze v případech, kdy je podporována vlastnost textu tvaru.

Když je součást **Buňka** nakonfigurována pro zadávání hodnoty do obrázku Excelu, může být svázána se zdrojem dat, který vrací hodnotu primitivního datového typu **Kontejner**, který představuje obrázek v binárním formátu. V tomto případě je hodnota zadána do obrázku Excelu jako obrázek.

> [!NOTE]
> Každý obrázek a tvar Excelu je považován za ukotvený svým levým horním rohem ke konkrétní buňce nebo rozsahu Excelu. Pokud chcete replikovat obrázek nebo tvar aplikace Excel, musíte nakonfigurovat buňku nebo rozsah, do kterých jsou ukotveny, jako replikovanou buňku nebo rozsah.

Chcete-li se dozvědět více o tom, jak vkládat obrázky a tvary, nahlédněte do části [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Součást konce stránky

Součást **Konec stránky** vynutí, aby Excel začal na nové stránce. Tato součást není vyžadována, pokud chcete použít výchozí stránkování aplikace Excel, ale měli byste ji použít, pokud chcete, aby aplikace Excel postupovala podle formátu elektronického výkaznictví pro vytvoření stránkování.

## <a name="footer-component"></a>Komponenta zápatí

Komponenta **Zápatí** se používá k vyplnění zápatí v dolní části vygenerovaného listu v sešitu aplikace Excel.

> [!NOTE]
> Tuto komponentu můžete přidat pro všechny komponenty **List** k určení různých zápatí pro různé listy ve vygenerovaném sešitu aplikace Excel.

Když konfigurujete jednotlivou komponentu **Zápatí**, můžete použít vlastnost **Vzhled záhlaví/zápatí** k určení stránek, pro které se komponenta používá. K dispozici jsou následující hodnoty:

- **Všechny** – Spustit nakonfigurovanou komponentu **Zápatí** pro všechny stránky nadřazeného listu aplikace Excel.
- **První** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro první stránku nadřazeného listu aplikace Excel.
- **Sudá** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro sudé stránky nadřazeného listu aplikace Excel.
- **Lichá** – Spustit nakonfigurovanou komponentu **Zápatí** pouze pro liché stránky nadřazeného listu aplikace Excel.

Pro jednu komponentu **List** můžete přidat několik komponent **Zápatí**, z nichž každá má pro vlastnost **Vzhled záhlaví/zápatí** jinou hodnotu. Tímto způsobem můžete vygenerovat různá zápatí pro různé typy stránek v listu aplikace Excel.

> [!NOTE]
> Zajistěte, aby každá komponenta **Zápatí**, kterou přidáte do jednoho **Listu**, měla pro vlastnost **Vzhled záhlaví/zápatí** jinou hodnotu. Jinak dojde k [chybě ověření](er-components-inspections.md#i16). Chybová zpráva, kterou obdržíte, vás upozorní na nekonzistenci.

Pod přidanou komponentu **Zápatí** přidejte požadované vnořené komponenty **Text\\Řetězec**, **Text\\DateTime** nebo jiný typ. Nakonfigurujte vazby pro tyto komponenty a určete, jak je vyplněno vaše zápatí stránky.

Můžete také použít speciální [formátovací kódy](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) ke správnému formátování obsahu vygenerovaného zápatí. Chcete-li se naučit používat tento přístup, postupujte podle pokynů v [příkladu 1](#example-1) dále v tomto tématu.

> [!NOTE]
> Při konfiguraci formátů ER nezapomeňte vzít v úvahu [limit](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) Excel a maximální počet znaků pro jedno záhlaví nebo zápatí.

## <a name="header-component"></a>Komponenta záhlaví

Komponenta **Záhlaví** se používá k vyplnění záhlaví v horní části vygenerovaného listu v sešitu aplikace Excel. Používá se stejně jako komponenta **Zápatí**.

## <a name="edit-an-added-er-format"></a>Úprava přidaného formátu elektronického výkaznictví

### <a name="update-a-template"></a>Aktualizace šablony

Můžete vybrat možnost **Aktualizovat z Excelu** na kartě podokna akcí **Importovat** a naimportovat aktualizovanou šablonu do upravitelného formátu elektronického výkaznictví. Během tohoto procesu bude šablona vybrané součásti **Excel\\Soubor** nahrazena novou šablonou. Obsah upravitelného formátu elektronického výkaznictví bude synchronizován s obsahem aktualizované šablony elektronického výkaznictví.

- Nová komponenta formátu elektronického výkaznictví bude automaticky vytvořena pro každý název Excelu, pokud komponenta formátu elektronického výkaznictví není nalezena v upravitelném formátu.
- Každá součást formátu elektronického výkaznictví bude odstraněna z upravitelného formátu elektronického výkaznictví, pokud pro ni nebude nalezen příslušný název Excelu.

> [!NOTE]
> Pokud chcete vytvořit volitelný prvek **List** v editovatelném formátu elektronického výkaznictví, nastavte možnost **Vytvořit prvek formátu listu Excel** na **Ano**.
>
> Pokud upravitelný formát elektronického výkaznictví původně obsahoval prvky **List**, doporučujeme nastavit možnost **Vytvořit prvek formátu listu Excel** na **Ano** při importu aktualizované šablony. V opačném případě budou všechny vnořené prvky původního prvku **List** vytvořeny od začátku. Proto budou všechny vazby znovu vytvořených prvků formátu ztraceny v aktualizovaném formátu elektronického výkaznictví.

![Možnost Vytvořit prvek formátu listu Excel v dialogovém okně Aktualizovat z Excelu](./media/er-excel-format-update-template.png)

Chcete-li se o této funkci dozvědět více, postupujte podle pokynů v části [Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Ověření formátu elektronického výkaznictví

Při ověření formátu elektronického výkaznictví, který lze upravit, se provede kontrola konzistence, aby se zajistilo, že název Excel bude přítomen v aktuálně používané šabloně Excel. O jakýchkoli nesrovnalostech budete informováni. V případě některých nesrovnalostí bude nabídnuta možnost automaticky opravit problémy.

![Chybové zprávy ověření](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Řízení průběhu výpočtu vzorců aplikace Excel

Když je generován odchozí dokument ve formátu sešitu Microsoft Excel, některé buňky tohoto dokumentu mohou obsahovat vzorce aplikace Excel. Když je aktivována funkce **Povolit použití knihovny EPPlus v rámci elektronického výkaznictví**, můžete určit, kdy přesně se vzorce vypočítají, změnou hodnoty [parametru](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Možnosti výpočtu** v šabloně aplikace Excel, která se používá:

- Když vyberete hodnotu **Automaticky**, přepočítají se všechny závislé vzorce pokaždé, když je generovaný dokument připojen novými rozsahy, buňkami atd.
    >[!NOTE]
    > To může způsobit problém s výkonem šablon aplikace Excel, které obsahují více souvisejících vzorců.
- Když vyberete hodnotu **Ručně**, nebudou vzorce přepočítány při generování dokumentu.
    >[!NOTE]
    > Přepočet vzorce je vynucen ručně, když je generovaný dokument otevřen k náhledu v aplikaci Excel.
    > Tuto možnost nepoužívejte, pokud konfigurujete cíl ER, který předpokládá použití vygenerovaného dokumentu bez jeho náhledu v aplikaci Excel (pro převod PDF, odeslání e-mailem atd.), protože generovaný dokument nemusí obsahovat hodnoty v buňkách obsahujících vzorce.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Příklad 1: Formátování obsahu zápatí

1. Použijte poskytnuté konfigurace ER ke [generování](er-generate-printable-fti-forms.md) dokumentu s volnou textovou fakturou (FTI), který lze tisknout.
2. Zkontrolujte zápatí vygenerovaného dokumentu. Všimněte si, že obsahuje informace o aktuálním čísle stránky a celkovém počtu stránek v dokumentu.

    ![Zkontrolujte zápatí vygenerovaného dokumentu ve formátu Excel](./media/er-fillable-excel-footer-1.gif)

3. V návrháři formátu ER [otevřete](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ukázkový formát ER pro kontrolu.

    Zápatí listu **faktury** je generováno na základě nastavení dvou komponent **Řetězec**, které jsou umístěny pod komponentou **Zápatí**.

    - První komponenta **Řetězec** vyplní následující speciální kódy formátování, aby donutila aplikaci Excel použít konkrétní formátování:

        - **&C** – Zarovnat text zápatí do středu.
        - **&"Segoe UI,Regular"&8** – Vložit text zápatí v písmu "Segoe UI Regular" písmo o velikosti 8 bodů.

    - Druhý komponent **Řetězec** vyplní text, který obsahuje aktuální číslo stránky a celkový počet stránek v aktuálním dokumentu.

    ![Zkontrolujte formát ER zápatí na stránce Návrhář formátů](./media/er-fillable-excel-footer-2.png)

4. Přizpůsobte ukázkový formát ER a upravte aktuální zápatí stránky:

    1. [Vytvořit](er-quick-start2-customize-report.md#DeriveProvidedFormat) odvozený formát **Faktura s volným textem (Excel) vlastní**, který je založen na vzorovém formátu ER.
    2. Přidejte první nový pár komponent **Řetězec** pro komponentu **Zápatí** listu **Faktura**:

        1. Přidejte komponentu **Řetězec**, která zarovná název společnosti vlevo a zobrazí jej v 8bodovém písmu "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).
        2. Přidejte komponentu **Řetězec** komponenta, která vyplňuje název společnosti (**model.InvoiceBase.CompanyInfo.Name**).

    3. Přidejte druhý nový pár komponent **Řetězec** pro komponentu **Zápatí** listu **Faktura**:

        1. Přidejte komponentu **Řetězec**, která zarovná datum zpracování vpravo a zobrazí jej v 8bodovém písmu "Segoe UI Regular" (**"&R&"Segoe UI,Regular"&8"**).
        2. Přidejte komponentu **Řetězec**, která vyplní datum zpracování ve vlastním formátu (**"&nbsp;&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Kontrola formátu ER zápatí na stránce Návrhář formátů](./media/er-fillable-excel-footer-3.png)

    4. [Vyplňte](er-quick-start2-customize-report.md#CompleteDerivedFormat) verzi konceptu odvozeného formátu ER **Faktura s volným textem (Excel) vlastní**.

5. [Nakonfigurujte](er-generate-printable-fti-forms.md#configure-print-management) správu tisku pro použití odvozeného formátu ER **Faktura s volným textem (Excel) vlastní** namísto ukázkového formátu ER.
6. Vygenerujte tisknutelný dokument FTI a zkontrolujte zápatí vygenerovaného dokumentu.

    ![Kontrola zápatí vygenerovaného dokumentu ve formátu Excel](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrh konfigurace pro generování sestav ve formátu OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel](modify-electronic-reporting-format-reapply-excel-template.md)

[Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel](tasks/er-horizontal-1.md)

[Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)

[Konfigurace elektronického výkaznictví pro doplňování dat do Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]