---
title: Vytvoření rozhraní pro provádění výrobního provozu
description: Toto téma vysvětluje, jak nakonfigurovat ovládací prvky formuláře, aby se na ně aplikovaly výchozí styly provádění výrobní plochy.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790883"
---
# <a name="style-the-production-floor-execution-interface"></a>Vytvoření rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nakonfigurovat ovládací prvky formuláře, aby se na ně aplikovaly výchozí styly provádění výrobní plochy.

## <a name="forms-and-dialogs"></a>Formuláře a dialogy

Styly lze na formulář nebo dialog použít pouze v případě, že jsou splněny následující požadavky:

- Pokud by se formulář měl podobat existujícímu formuláři průběhu sestavy, musí název vašeho formuláře nebo dialogu začínat řetězcem `JmgProductionFloorExecutionCustomInputDialog`.
- Formulář nebo dialog může obsahovat podrobnou část formuláře. Chcete-li na něj použít styly, musí název části formuláře podrobností začínat řetězcem `JmgProductionFloorExecutionCustomDetailsDialog`.
- Pokud má mít formulář nebo dialogové okno jednoduché zobrazení, musí název jednoduchého zobrazení začínat řetězcem `JmgProductionFloorExecutionCustomDialog`. Příklady formulářů, které mají jednoduché zobrazení, zahrnují počáteční formulář a formulář nepřímé aktivity.
- Všechny ovládací prvky v dialogu musejí být konfigurovány tak, jak je popsáno v tomto tématu.

> [!IMPORTANT]
> Funkce uvedené v prvních dvou odrážkách tohoto seznamu vyžadují Supply Chain Management verze 10.0.19 nebo novější.

Styly lze na tlačítko **OK** v dialogu použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `OkButtonGroup`.

Styly lze na tlačítko **Zrušit** v dialogovém okně použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `CancelButtonGroup`.

### <a name="header"></a>Záhlaví

Následující obrázek ukazuje typické záhlaví formuláře nebo dialogu.

![Typické záhlaví formuláře nebo dialogu.](media/pfe-styles-header.png "Typické záhlaví formuláře nebo dialogu")

V aplikaci Visual Studio jsou záhlaví vytvořena pomocí struktury, jejíž příklad je znázorněn na následujícím obrázku.

![Typická struktura kódu pro vytvoření záhlaví.](media/pfe-styles-header-code-structure.png "Typická struktura kódu pro vytvoření záhlaví")

Chcete-li do záhlaví přidat text, použijte kód, který vypadá jako následující příklad.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Při psaní kódu záhlaví použijte následující pravidla:

- Název hlavní skupiny musí být `TableRowHeaderGroup`.
- Každý blok textu (oddělený odrážkami) musí začínat řetězcem `HeaderFieldWithSeparatorText`.
- Poslední textový název musí začínat řetězcem `HeaderFieldText`.
- `CaptionImage` lze přeskočit.

### <a name="progress-indicator"></a>Indikátor pokroku

Můžete zahrnout indikátor průběhu, který je zobrazen napravo od záhlaví. Následující obrázek ukazuje indikátor průběhu.

![Typický indikátor průběhu.](media/pfe-styles-header-progress.png "Typický indikátor průběhu")

Aby se zobrazil indikátor průběhu, musí se textové pole jmenovat `ShowProgress`.

## <a name="grid"></a>Mřížka

Styly se použijí automaticky. Není vyžadována žádná konkrétní konfigurace.

Mřížka by měla mít styl `TabularView` a metodu `run()` ve vlastním formuláři musíte přepsat, protože nová mřížka zatím není podporována. Přidejte následující kód.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Chcete-li obnovit data v hlavním zobrazení, možná budete chtít použít něco jako `this.parmParentForm().updateLayout();` v metodě `click` vaší akce. (Podívejte se například na třídu `JmgProductionFloorExecutionReportFeedbackAction`.) Jen se ujistěte, že nastavíte `parmDataSource` v metodě `init` vašeho nového formuláře (`formCaller.parmDataSource(this.dataSource(1));`). Podívejte se například na formulář `JmgProductionFloorExecutionMainGrid`.

## <a name="card-view"></a>Zobrazení karet

Styly lze na ovládací prvky zobrazení karty použít pouze v případě, že jsou splněny následující požadavky:

- Každé zobrazení karty je obsaženo ve skupině formulářů.
- Název skupiny začíná na `CardGroup` (například `CardGroupJobsView`).

Následující obrázek ukazuje pohled na kartu, která neobsahuje žádné ovládací prvky.

![Pohled na kartu bez prvků.](media/pfe-styles-empty-card.png)

Následující ilustrace ukazují zobrazení karty, která neobsahují žádné ovládací prvky.

![Karta s prvky, které ukazují Hz.](media/pfe-styles-elements.png)

![Karta s prvky pro požadavek na údržbu.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Vizitka

Styly lze na ovládací prvky vizitky použít pouze v případě, že jsou splněny následující požadavky:

- Každá vizitka je obsažena ve skupině formulářů.
- Název skupiny začíná na `BusinessCardGroup` (například `BusinessCardGroupJobsList`).

Nastavte na vizitce následující vlastnosti:

- **Style:** *seznam*
- **Extended style:** *cardList*
- **Multi Select:** *Ne*
- **Show Col Labels:** *Ne*

![Vizitka.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Přepínač

Styly lze na přepínače použít pouze v případě, že jsou splněny následující požadavky:

- Každý přepínač je obsažen ve skupině formulářů.
- Název skupiny začíná řetězcem `RadioTextBelow` nebo `RadioTextRight`, podle toho, kde chcete text zobrazit.

Nastavte na přepínači následující vlastnosti:

- **Toggle button:** *Zapnout*
- **Toggle value:** *Zapnuto*, pokud má být přepínač vybraný, jinak *Vypnuto*

Následující obrázek ukazuje příklad, kde se text zobrazuje pod přepínači.

![Přepínače s textem pod sebou.](media/pfe-styles-radio-text-below.png)

Následující obrázek ukazuje příklad, kde se text zobrazuje napravo od přepínačů.

![Přepínače s textem vpravo.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Přepínače v Internet Explorer

Styly přepínačů nejsou v Internet Explorer podporovány. Následující obrázek znázorňuje, jak přepínače vypadají v Internet Explorer.

![Přepínače v Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Tlačítka

Styly lze na tlačítka použít pouze v případě, že jsou splněny následující požadavky:

- Každá skupina tlačítek je obsažena ve skupině formulářů. Všechna tlačítka ve skupině budou mít stejný styl.
- Neexistují žádné požadavky na název skupiny.

Nastavte na tlačítkách následující vlastnosti:

- **Button Display:** *TextWithImageLeft*
- **Normal Image:** Tato vlastnost nemůže být prázdná. Na příklad použijte *CoffeeScript*.
- **Text:** Tato vlastnost nemůže být prázdná. Na příklad použijte *Začátek přestávky*.
- **Width:** *Automaticky* nebo *SizeToContent*
- **Height:** *Automaticky* nebo *SizeToContent*

### <a name="primary-button"></a>Primární tlačítko

Styly lze na primární tlačítko použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `DefaultButtonGroup` nebo `PrimaryButtonGroup` (například `DefaultButtonGroup10`).

![Primární tlačítko.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundární tlačítko

Styly lze na sekundární tlačítko použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Skupina se jmenuje **Pravý panel** nebo název skupiny začíná řetězcem `SecondaryButtonGroup`.

![Sekundární tlačítko.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Tlačítko třetí skupiny

Styly lze na tlačítko třetí skupiny použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Skupina se jmenuje **Levý panel** nebo název skupiny začíná řetězcem `ThirdButtonGroup`.

![Tlačítko třetí skupiny.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Tlačítko čtvrté skupiny

Styly lze na tlačítko čtvrté skupiny použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `FourthButtonGroup`.

Nastavte na tlačítku následující vlastnosti:

- **Button Display:** *TextOnly*
- **Normal Image:** Tato vlastnost musí být prázdná.
- **Text:** Tato vlastnost nemůže být prázdná. Například použijte *Pohled* nebo *Upravit*.
- **Width:** *Automaticky*
- **Height:** *Automaticky*

![Tlačítko čtvrté skupiny.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Ploché tlačítko

Styly lze na ploché tlačítko použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `FlatButtonGroup`.

Nastavte na tlačítku následující vlastnosti:

- **Button Display:** *ImageOnly*
- **Normal Image:** Tato vlastnost nemůže být prázdná. Na příklad použijte *CoffeeScript*.
- **Text:** Tato vlastnost musí být prázdná.
- **Width:** *Automaticky* nebo *SizeToContent*
- **Height:** *Automaticky* nebo *SizeToContent*

![Ploché tlačítko.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Tlačítko Pokračovat

Styly lze na tlačítko Pokračovat použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `ContinueButtonGroup`.

Nastavte na tlačítku následující vlastnosti:

- **Button Display:** *ImageOnly*
- **Normal Image:** *Dopředu*
- **Text:** Tato vlastnost musí být prázdná.
- **Width:** *Automaticky* nebo *SizeToContent*
- **Height:** *Automaticky* nebo *SizeToContent*

![Tlačítko Pokračovat.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Pole se seznamem

Pole se seznamem je kombinací tří ovládacích prvků: ovládacího prvku vstupu, tlačítka, které vymaže ovládací prvek vstupu, a tlačítka, které spouští vyhledávání.

Styly lze na pole se seznamem použít pouze v případě, že jsou splněny následující požadavky:

- Tlačítko se seznamem je obsaženo ve skupině formulářů.
- Název skupiny začíná řetězcem `Combobox`.
- Uvnitř skupiny je prvním ovládacím prvkem `AxFormStringControl`. Tento ovládací prvek zobrazuje aktuální hodnotu a je to místo, kde uživatel zadá požadovanou hodnotu.
- Druhý ovládací prvek je `CommonButton` a jeho název začíná řetězcem `ClearButton`. Toto tlačítko musí obsahovat kód, který používá vlastnost `enable` k zobrazení nebo skrytí tlačítka. Chcete-li například k zobrazení nebo skrytí tlačítka **Vymazat**, zatímco uživatel zadává informace do vstupního ovládacího prvku, můžete použít následující kód.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Měli byste mít jednu metodu, kde jsou data nastavena ve vstupním ovládacím prvku. Aktivujte tlačítko **Vymazat** v této metodě. Následuje příklad.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Použijte následující kód pro metodu `clicked` tlačítka **Vymazat**.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Nastavte hodnotu vstupního ovládacího prvku `AxFormStringControl`, když je formulář inicializován pomocí metody `init`. Pokud hodnota není prázdná, aktivovat tlačítko **Vymazat**. Pokud hodnota je prázdná, deaktivovat tlačítko **Vymazat**.

- Třetí ovládací prvek je `CommonButton` a jeho název začíná řetězcem `SearchButton`.

Následující obrázek ukazuje dva ovládací prvky pole se seznamem. Pole se seznamem vlevo obsahuje prázdné textové pole a tlačítko **Vymazat** je deaktivováno. Pole se seznamem vpravo obsahuje text v textovém poli a tlačítko **Vymazat** je aktivováno.

![Pole se seznamem s tlačítkem Vymazat a bez něj.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Rychlý filtr

Ovládací prvek rychlého filtru přidá na stránku vyhledávací pole. Styly můžete použít na rychlý filtr, pokud jsou splněny následující požadavky:

- Rychlý filtr je obsažen ve skupině formulářů.
- Název skupiny začíná řetězcem `SearchInputGroup`.
- Uvnitř skupiny je prvním ovládacím prvkem `QuickFilter`. (Tento ovládací prvek je místo, kde uživatel zadá hledaný řetězec.)
- Druhý ovládací prvek je `FormStaticTextControl` a jmenuje se `NumberOfResults`. (Tento ovládací prvek je volitelný. Pokud existuje, zobrazuje počet nalezených položek.)
- Třetí ovládací prvek je `CommonButton` a jeho název začíná řetězcem `ClearButton`.

Následující obrázek ukazuje dva ovládací prvky rychlého filtru. Rychlý filtr vlevo má prázdný rychlý filtr a počet výsledků není vidět. Rychlý filtr vpravo obsahuje vyhledávací řetězec a zobrazuje počet výsledků.

![Příklady rychlého ovládání filtru s vyhledávacím řetězcem a bez něj.](media/pfe-styles-quick-filter.png "Příklady rychlého ovládání filtru s vyhledávacím řetězcem a bez něj")

## <a name="center-align-elements-on-a-tab"></a>Prvky zarovnané na kartě na střed

Chcete-li zarovnat prvky na střed karty, název skupiny musí začínat řetězcem `TabContentGroup` a skupina musí mít následující vlastnosti:

- **Width Mode:** `SizeToAvailable`
- **Height Mode:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Zarovnání mřížky, části podrobností a rychlého filtru

Chcete-li uspořádat přizpůsobenou mřížku, část podrobností a rychlý filtr tak, aby připomínaly standardní návrh, mějte při sestavování všech věcí na paměti následující body:

- Pokud má mřížka rychlý filtr, mřížka i rychlý filtr by měly být uvnitř skupiny, jejíž název začíná řetězcem `GridGroup`.
- Chcete-li na část podrobností použít styly, musí název skupiny začínat řetězcem `DetailInformationGroup`.

Následující obrázek ukazuje typickou mřížku, která obsahuje rychlý filtr a část podrobností vpravo.

![Typická mřížka, která obsahuje rychlý filtr a část podrobností.](media/pfe-styles-align-grid.png "Typická mřížka, která obsahuje rychlý filtr a část podrobností")

V aplikaci Visual Studio je možné mřížku, část podrobností a rychlý filtr vytvořit pomocí struktury, jejíž příklad je znázorněn na následujícím obrázku.

![Typická mřížka, která zarovná mřížku, část podrobností a rychlý filtr.](media/pfe-styles-header-code-structure2.png "Typická mřížka, která zarovná mřížku, část podrobností a rychlý filtr")

## <a name="additional-resources"></a>Další prostředky

- [Přizpůsobení rozhraní pro provádění výrobního provozu](production-floor-execution-customize.md)
- [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
