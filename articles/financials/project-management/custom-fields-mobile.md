---
title: Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systéech iOS a Android
description: Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2019
ms.locfileid: "1617989"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systéech iOS a Android

[!include [banner](../includes/banner.md)]

Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí. Jsou zde pokryta následující témata:

- Různé datové typy, které rozhraní vlastních polí podporuje
- Jak v záznamech časového rozvrhu zobrazit pole jen pro čtení nebo upravitelná pole a uložit hodnoty zadané uživatelem zpět do databáze
- Jak zobrazit pole určená jen pro čtení v záhlaví časového rozvrhu
- Jak integrovat jinou vlastní obchodní logiku pro zadávání výchozích hodnot v polích a provádět další ověření

## <a name="audience"></a>Cílová skupina

Toto téma je určeno pro vývojáře, kteří integrují svá vlastní pole do mobilní aplikace Microsoft Dynamics 365 Project Timesheet, která je k dispozici pro systémy Apple iOS a Google Android. Předpokladem je, že čtenáři jsou obeznámeni s vývojem X ++ a funkcionalitou časových rozvrhů projektu.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Kontrakt dat – třída TSTimesheetCustomField X + +

Třída **TSTimesheetCustomField** je třídou kontraktu dat X ++, která představuje informace o vlastním poli pro funkcionalitu časového rozvrhu. Seznamy objektů vlastního pole jsou předány jak na kontrakt dat TSTimesheetDetails, tak na kontrakt dat TSTimesheetEntry pro zobrazení vlastních polí v mobilní aplikaci.

- **TSTimesheetDetails** – Kontrakt záhlaví časového rozvrhu.
- **TSTimesheetEntry** – Kontrakt transakce časového rozvrhu Skupiny těchto objektů, které mají stejné informace o projektu a hodnotu **timesheetLineRecId** tvoří jeden řádek.

### <a name="fieldbasetype-types"></a>fieldBaseType (typy)

Vlastnost **FieldBaseType** na objektu **TsTimesheetCustom** určuje typ pole, které se zobrazí v aplikaci. Jsou podporovány následující **typy** hodnot.

| Hodnota typů | Typ              | Poznámky |
|-------------|-------------------|-------|
| 0           | Řetězec (a výčet) | Pole se zobrazí jako textové pole. |
| 1           | Celé číslo           | Hodnota se zobrazí jako číslo bez desetinných míst. |
| 2           | Reálný              | Hodnota se zobrazí jako číslo s desetinnými místy.<p>Chcete-li v aplikaci zobrazit reálnou hodnotu jako měnu, použijte vlastnost **fieldExtenededType**. Pomocí vlastnosti **numberOfDecimals** můžete nastavit počet zobrazených desetinných míst.</p> |
| 3           | Datum              | Formáty data jsou určeny nastavením **formátu data, času a čísel** uživatele, které je uvedeno v části **Předvolby jazyka a země/oblasti** pod volbou **Možnost uživatele**. |
| 4           | Logická hodnota           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Není-li na objektu **TSTimesheetCustomField** zadána vlastnost **stringOptions**, je uživateli poskytnuto pole s volným textem.

    Vlastnost **stringLength** lze použít k nastavení maximální délky řetězce, kterou mohou uživatelé zadat.

- Je- li vlastnost **stringOptions** zadána na objektu **TSTimesheetCustomField**, budou tyto prvky seznamu jediné hodnoty, které mohou uživatelé vybrat pomocí tlačítek možností (přepínačů).

    V tomto případě může pole řetězce sloužit jako hodnota výčtu pro účely zadání uživatele. Chcete-li hodnotu uložit do databáze jako výčet, před uložením do databáze pomocí chain of command ručně, namapujte hodnotu řetězce zpět na hodnotu výčtu (příklad naleznete dále v tomto tématu v části „Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze“).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Tato vlastnost slouží k formátování reálných hodnot jako měny. Tento přístup je použitelný pouze v případě, že hodnota **fieldBaseType** je **reálná**.

- **TSCustomFieldExtendedType: None** – Není použito žádné formátování.
- **TSCustomFieldExtendedType::Currency** – Naformátuje hodnotu jako měnu.

    Je-li formátování měny aktivní, pole **stringValue** lze použít k předání kódu měny, který by měl být zobrazen v aplikaci. Hodnota je pouze pro čtení.

    Pole **realValue** obsahuje peněžní částku, která má být uložena do databáze.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Pomocí této vlastnosti můžete určit, kde se má vlastní pole zobrazit v aplikaci.

- **TSCustomFieldSection::Header** – Pole se zobrazí v části **Zobrazit více podrobností** v aplikaci. Tato pole jsou vždy pouze ke čtení.
- **TSCustomFieldSection::Line** – Pole se zobrazí po všech předdefinovaných polí řádků v záznamech časového rozvrhu. Tato pole mohou být upravitelná nebo jen pro čtení.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Tato vlastnost identifikuje pole, když hodnoty, které aplikace poskytuje, jsou uloženy zpět do databáze.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Tato vlastnost identifikuje pole, když hodnoty, které aplikace poskytuje, jsou uloženy zpět do databáze.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Chcete-li určit, že pole v části záznamu časového rozvrhu by mělo být pro uživatele upravitelné, nastavte tuto vlastnost na **Ano**. Nastavením vlastnosti na **Ne** nastavíte pole jen pro čtení.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Chcete-li určit, že pole v části záznamu časového rozvrhu by mělo být pro uživatele povinné, nastavte tuto vlastnost na **Ano**.

### <a name="label-str"></a>label (str)

Tato vlastnost určuje popisek zobrazený vedle pole v aplikaci.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Tuto vlastnost lze použít pouze tehdy, když je **fieldBaseType** nasteveno na **Řetězec**. Když je nastavena hodnota **stringOptions**, hodnoty řetězců, které jsou k dispozici pro výběr prostřednictvím tlačítek možností (přepínačů), jsou určeny řetězci v seznamu. Nejsou-li zadány žádné řetězce, bude záznam s volným textem v poli řetězce povolen (příklad naleznete dále v tomto tématu v části „Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze“).

### <a name="stringlength-int"></a>stringLength (int)

Tato vlastnost určuje maximální délku pole řetězců. Lze ji použít pouze tehdy, když je **fieldBaseType** nasteveno na **Řetězec**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Tato vlastnost určuje počet desetinných míst, která se zobrazí u reálného pole. Lze ji použít pouze tehdy, když je **fieldBaseType** nasteveno na **Reálný**.

### <a name="ordersequence-int"></a>orderSequence (int)

Tato vlastnost řídí pořadí, ve kterém se vlastní pole zobrazí v aplikaci v případě, že je zadáno více než jedno vlastní pole. Pole s nižšími čísly jsou zobrazena jako první.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

U polí typu **Logická hodnota** předává tato vlastnost logickou hodnotu pole mezi serverem a aplikací.

### <a name="guidvalue-guid"></a>guidValue (guid)

U polí typu **GUID** předává tato vlastnost hodnotu identifikátoru GUID pole mezi serverem a aplikací.

### <a name="int64value-int64"></a>int64Value (Int64)

U polí typu **Int64** předává tato vlastnost hodnotu Int64 pole mezi serverem a aplikací.

### <a name="intvalue-int"></a>intValue (int)

U polí typu **Int** předává tato vlastnost hodnotu int pole mezi serverem a aplikací.

### <a name="realvalue-real"></a>realValue (Real)

U polí typu **Reálné** předává tato vlastnost reálnou hodnotu pole mezi serverem a aplikací.

### <a name="stringvalue-str"></a>stringValue (str)

U polí typu **Řetězec** předává tato vlastnost hodnotu řetězce pole mezi serverem a aplikací. Používá se také pro pole typu **Reálné**, která jsou formátována jako měna. Pro tato pole se vlastnost používá k předání kódu měny do aplikace.

### <a name="datevalue-date"></a>dateValue (date)

U polí typu **Datum** předává tato vlastnost hodnotu data pole mezi serverem a aplikací.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zobrazení a uložení vlastního pole v části záznamu časového rozvrhu

Níže je snímek obrazovky z mobilní aplikace zobrazující vytvoření záznamu časového rozvrhu. Zobrazuje předpřipravená pole a vlastní pole v části časového záznamu s názvem Testovací řetězec s již nastavenou hodnotou výčtu Druhá možnost.

![Vlastní pole testovacího řetězce v aplikaci](media/timesheet-entry.jpg)



Níže je snímek obrazovky z mobilní aplikace zobrazující uživatele, který vybere jednu z možností výčtu dostupných pro vlastní pole Testovací řetězec.  Tyto dvě možnosti jsou První možnost a Druhá možnost, které jsou zobrazeny jako přepínací tlačítka. Aktuálně je vybrána druhá možnost.

![Tlačítka možností (přepínače) pro vlastní pole Testovací řetězec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Rozšíření tabulky TSTimesheetLine tak, aby obsahovala vlastní pole

V typických scénářích je pravděpodobné, že data pro vlastní pole v části záznamu časového rozvrhu budou uložena do tabulky TSTimesheetLine. Lze však použít i jiné tabulky, pokud je možné data načíst na základě poskytnutého záznamu TSTimesheetTrans, nebo pokud nemá specifický kontext záznamu (pokud je například pole v parametrech projektu nastaveno na hodnotu jen pro čtení).

Všimněte si, že vlastní pole nemusí mít žádné podpůrné záznamy databáze. Lze je dynamicky generovat na základě logiky X ++. Tento přístup může být užitečný ve scénářích jen pro čtení (nahlédněte do části „Použití chain of command v třídě TSTimesheetDetails a metodě buildCustomFieldListForHeader pro vyplnění podrobností časového rozvrhu, kde je uveden přiklad dynamicky generovaných hodnot vlastních polí).

Níže je snímek obrazovky stromu aplikačních objektů z aplikace Visual Studio. Zobrazuje rozšíření tabulky TSTimesheetLine s polem TestLineString přidaným jako vlastní pole.

![Řetězec řádku](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Použití chain of command v metodě buildCustomFieldList třídy TSTimesheetSettings pro zobrazení pole v části záznamu časového rozvrhu

Tento kód řídí nastavení zobrazení pro pole v aplikaci. Například řídí typ pole, popisek, zda je pole povinné a v jaké části se pole zobrazí.

V následujícím příkladu je pole řetězce uvedeno v časových záznamech. Toto pole obsahuje dvě možnosti, **První možnost** a **Druhá možnost**, které jsou k dispozici prostřednictvím tlačítek možností (přepínačů). Pole v aplikaci je přidruženo k poli **TestLineString**, které je přidáno do tabulky TSTimesheetLine.

Všimněte si použití metody **TSTimesheetCustomField::newFromMetatdata()** pro zjednodušení inicializace vlastností vlastních polí: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**. Tyto parametry lze také nastavit ručně podle potřeby.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Použití chain of command v metodě buildCustomFieldListForEntry třídy TSTimesheetEntry pro zadání hodnot v záznamu časového rozvrhu

Metoda **buildCustomFieldListForEntry** slouží k zadávání hodnot do uložených řádků časového rozvrhu v mobilní aplikaci. Bere záznam TSTimesheetTrans jako parametr. Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Použití chain of command v třídě TSTimesheetEntryService pro uložení záznamu časového rozvrhu z aplikace zpět do databáze

Chcete-li uložit vlastní pole zpět do databáze v typickém použití, je nutné rozšířit více metod:

- Metoda **timesheetLineNeedsUpdating** slouží k určení, zda byl záznam řádku uživatelem v aplikaci změněn a musí být uložen do databáze. Pokud není problémem výkonnost, lze tuto metodu zjednodušit, aby vždy vracela hodnotu **true**.
- Metody **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** mohou být rozšířeny tak, aby do databázového záznamu TSTimesheetLine zadávaly hodnoty z TSTimesheetEntry ze zadaného záznamu kontraktu dat. V následujícím příkladu si všimněte, jak se provádí mapování mezi polem databáze a polem záznamu ručně pomocí kódu X ++.
- Metodu **populateTimesheetWeekFromEntry** lze rovněž rozšířit, pokud vlastní pole, které je mapováno na objekt **TSTimesheetEntry**, musí zapisovat zpět do tabulky tabulky databáze TSTimesheetLineweek.

> [!NOTE]
> Následující příklad ukládá hodnotu **firstOption** nebo **secondOption** vybranou uživatelem do databáze jako neupravenou hodnotu řetězce. Je-li pole databáze typem pole **Výčet**, lze tyto hodnoty ručně namapovat na hodnotu výčtu a poté je uložit do pole výčtu v tabulce databáze.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zobrazení vlastního pole v části záhlaví časového rozvrhu

Níže je uveden snímek obrazovky z mobilní aplikace uživatele, který si prohlíží časový rozvrh. Tlačítko Další informace bylo vybráno v pravém horním rohu k zobrazení možnosti Zobrazit další podrobnosti.  

![Příkaz Zobrazit další podrobnosti](media/show-more.png)



Níže je uveden snímek obrazovky z mobilní aplikace s částí časového rozvrhu Další. Do části záhlaví časového rozvrhu bylo přidáno vlastní pole s názvem Míra využití tohoto časového rozvrhu (vypočítané vlastní pole). U vlastního pole je nastavena hodnota 0,667 jen pro čtení.

![Část Další](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Rozšíření tabulky TSTimesheetTable tak, aby obsahovala vlastní pole

V typických scénářích je pravděpodobné, že data pro vlastní pole v části záhlaví budou načtena z tabulky TSTimesheetHeader. Lze však použít i jiné tabulky, pokud je možné data načíst na základě poskytnutého záznamu TSTimesheetTable, nebo pokud nemá specifický kontext záznamu (pokud je například pole v parametrech projektu nastaveno na hodnotu jen pro čtení).

Všimněte si, že vlastní pole nemusí mít žádné podpůrné záznamy databáze. Lze je dynamicky generovat na základě logiky X ++. Tento přístup je uveden v následujícím příkladu.

Pole v části záhlaví jsou v aplikaci vždy jen pro čtení.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Použití chain of command v metodě buildCustomFieldList třídy TSTimesheetSettings pro zobrazení pole v části header

Tento kód řídí nastavení zobrazení pro pole v aplikaci. Například řídí typ pole, popisek, zda je pole povinné a v jaké části se pole zobrazí.

Následující příklad ukazuje vypočítanou hodnotu v části záhlaví v aplikaci.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Použití chain of command v metodě buildCustomFieldListForHeader třídy TSTimesheetDetails pro vyplnění podrobností časového rozvrhu

Metoda **buildCustomFieldListForHeader** slouží k vyplnění podrobností záhlaví časového rozvrhu v mobilní aplikaci. Bere záznam TSTimesheetTable jako parametr. Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci. Následující příklad nečte žádné hodnoty z databáze. Místo toho používá logiku X ++ k vygenerování vypočtené hodnoty, která je pak zobrazena v aplikaci.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Další možnosti konfigurovatelnosti a rozšiřitelnosti

### <a name="adding-additional-validation-for-the-app"></a>Přidání dalšího ověřování pro aplikaci

Existující logika pro funkci časového rozvrhu na úrovni databáze bude stále fungovat očekávaným způsobem. Chcete-li přerušit dokončení operací uložení nebo odeslání a zobrazit určitou chybovou zprávu, můžete ke kódu přidat **throw error("message to user")** prostřednictvím rozšíření chain of command. Zde jsou tři příklady užitečných metod rozšiřitelnosti:

- Pokud **validateWrite** v tabulce TSTimesheetLine vrátí během operace uložení hodnotu **false** pro řádek časového rozvrhu, zobrazí se v mobilní aplikaci chybová zpráva.
- Pokud **validateSubmit** v tabulce TSTimesheetTable vrátí během odeslání časového rozvrhu v aplikaci hodnotu **false**, zobrazí se uživateli chybová zpráva.
- Logika, která vyplňuje pole (například **Vlastnost řádku**) během metody **insert** v tabulce TSTimesheetLine, bude stále spuštěna.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skrytí a označení předdefinovaných polí jako jen pro čtení pomocí konfigurace

Z parametrů projektu můžete změnit předdefinovaná pole na jen pro čtení nebo skrytá v mobilní aplikaci. Nastavte možnosti v části **Mobilní časové rozvrhy** na kartě **Časový rozvrh** na stránce **Parametry modulu Řízení a účetnictví projektu**.

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Změna aktivit, které jsou k dispozici pro výběr prostřednictvím rozšíření

Aktivity, které jsou k dispozici pro výběr pro projekt, jsou vyplněny pomocí metod **getActivitiesForProject()** a **getActivityQuery()** ve třídě **TsTimesheetProjectService**. Pomocí chain of command můžete toto chování změnit tak, aby vyhovovalo vašemu obchodnímu scénáři pro aktivity, které jsou k dispozici pro výběr pro určitý projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Zadání výchozí kategorie projektu do záznamů časového rozvrhu

Zadání výchozí kategorie projektu do záznamů časového rozvrhu se uskutečňuje na třech úrovních. Pomocí chain of command můžete rozšířit chování na některé nebo všechny tyto úrovně a dosáhnout požadovaného chování. Použije se následující hierarchie:

1. Aplikace se pokusí vložit výchozí kategorii ze zdroje projektu. Tato výchozí kategorie se nastavuje v metodách **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** ve třídě **TSTimesheetSettingsService**.
2. Není-li výchozí kategorie zadána na úrovni zdroje projektu, aplikace se pokusí ji načíst z aktivity projektu. Tato výchozí kategorie se nastavuje v metodě **getActivitiesForProject** ve třídě **TSTimesheetProjectService**.
3. Není-li výchozí kategorie zadána na úrovni aktivity projektu, vezme se výchozí kategorie z parametrů projektu. Tato výchozí kategorie se nastavuje v metodě **getProjectDetailsbyRule** ve třídě **TSTimesheetProjectService**.
