---
title: Přizpůsobení rozhraní pro provádění výrobního provozu
description: Tento článek vysvětluje, jak rozšířit aktuální formuláře nebo vytvořit nové formuláře a tlačítka pro rozhraní provádění výrobního provozu.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845975"
---
# <a name="customize-the-production-floor-execution-interface"></a>Přizpůsobení rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Vývojáři mohou rozšířit aktuální formuláře nebo vytvořit své vlastní formuláře a tlačítka pro rozhraní provádění výrobního provozu. Po přidání kódu pro tyto nové prvky je mohou administrátoři nebo manažeři výroby snadno přidat do rozhraní pomocí standardních konfiguračních ovládacích prvků.

Zde jsou například některá z možných řešení, pokud jsou v hlavním formuláři potřeba nové sloupce:

- Rozšiřte formulář `JmgProductionFloorExecutionMainGrid` a přidejte požadovaná pole.
- Vytvořte nový formulář a přidejte jej jako nové hlavní zobrazení (kartu).

## <a name="add-a-new-button-action"></a>Přidání nového tlačítka (akce)

Chcete-li přidat nové tlačítko (akci), postupujte podle těchto kroků a vytvořte třídu, která implementuje vaši vlastní akci.

1. Vytvořte novou třídu s názvem `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kde:

    - `<ExtensionPrefix>` jedinečně identifikuje vaše řešení, obvykle pomocí názvu vaší společnosti.
    - `<ActionName>` je jedinečný název třídy. Obvykle identifikuje druh akce.

1. Nová třída musí rozšířit třídu `JmgProductionFloorExecutionAction`.
1. Přepište všechny potřebné metody.

Podívejte se například na kód následujících tříd:

- `JmgProductionFloorExecutionBreakAction` – Třída pro jednoduchou akci, která nepotřebuje žádné záznamy.
- `JmgProductionFloorExecutionReportFeedbackAction` – Třída, která poskytuje složitější funkce.

Po dokončení bude nové tlačítko (akce) automaticky uvedeno na seznamu **Návrh karet** v aplikaci Microsoft Dynamics 365 Supply Chain Management. Tam jej můžete vy (nebo správce nebo vedoucí výroby) snadno přidat na primární nebo sekundární panel nástrojů, stejně jako můžete přidat standardní tlačítka. Návod najdete v tématu [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Přidání nového hlavního zobrazení

1. Vytvořte nový formulář, který má požadované prvky a funkce. Upozorňujeme, že tento formulář je nový formulář, nikoli rozšíření. Pojmenujte formulář jako `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kde:

    - `<ExtensionPrefix>` jedinečně identifikuje vaše řešení, obvykle pomocí názvu vaší společnosti.
    - `<FormName>` je jedinečný název formuláře.

1. Vytvořte položku nabídky s názvem `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Vytvořte rozšíření s názvem `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kde je metoda `getMainMenuItemsList` rozšířena přidáním nové položky nabídky do seznamu. Následující kód znázorňuje příklad.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Po dokončení bude nové hlavní zobrazení automaticky uvedeno v rozvíracím seznamu **Hlavní zobrazení** na stránce **Návrh karet** v Supply Chain Management. Tam jej můžete vy (nebo správce nebo vedoucí výroby) snadno přidat na nové nebo stávající karty, stejně jako můžete přidat standardní hlavní zobrazení. Návod najdete v tématu [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Přidání zobrazení podrobností

1. Vytvořte nový formulář, který má požadované prvky a funkce. Upozorňujeme, že tento formulář je nový formulář, nikoli rozšíření. Pojmenujte formulář jako `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kde: 

    - `<ExtensionPrefix>` jedinečně identifikuje vaše řešení, obvykle pomocí názvu vaší společnosti.
    - `<FormName>` je jedinečný název formuláře.

1. Vytvořte položku nabídky s názvem `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Vytvořte rozšíření s názvem `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, kde je metoda `getDetailsMenuItemList` rozšířena přidáním nové položky nabídky do seznamu.

Po dokončení bude nové zobrazení podrobností automaticky uvedeno v rozvíracím seznamu **Zobrazení podrobností** na stránce **Návrh karet** v Supply Chain Management. Tam jej můžete vy (nebo správce nebo vedoucí výroby) snadno přidat na nové nebo stávající karty, stejně jako můžete přidat standardní zobrazení podrobností. Návod najdete v tématu [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Přidání numerické klávesnice do formuláře nebo dialogu

Následující příklad ukazuje, jak do formuláře přidat numerické klávesnice.

1. Počet ovladačů numerické klávesnice, které každý formulář obsahuje, se musí rovnat počtu numerických klávesnic v daném formuláři.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Nastavte chování každého ovladače numerické klávesnice a připojte každý ovladač numerické klávesnice k části formuláře s numerickou klávesnicí.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Použití numerické klávesnice jako vyskakovacího dialogu

Následující příklad ukazuje jeden způsob, jak nastavit ovladač numerické klávesnice pro vyskakovací dialog.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Následující příklad ukazuje jeden způsob, jak zavolat vyskakovací dialog numerické klávesnice.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Přidání ovládacích prvků data a času do formuláře nebo dialogu

Tato část ukazuje, jak přidat ovládací prvky data a času do formuláře nebo dialogu. Dotekové ovládání data a času umožňuje pracovníkům specifikovat data a časy. Následující snímky obrazovky ukazují, jak se ovládací prvky obvykle zobrazují na stránce. Ovládací prvek času nabízí 12hodinovou i 24hodinovou verzi; zobrazená verze bude odpovídat předvolbám nastaveným pro uživatelský účet, pod kterým rozhraní běží.

![Příklad ovládacího prvku kalendářního data.](media/pfe-customize-date-control.png "Příklad ovládacího prvku kalendářního data")

![Příklad ovládacího prvku času s 12hodinovým časem.](media/pfe-customize-time-control-12h.png "Příklad ovládacího prvku času s 12hodinovým časem")

![Příklad ovládacího prvku času s 24hodinovým časem.](media/pfe-customize-time-control-24h.png "Příklad ovládacího prvku času s 24hodinovým časem")

Následující postup ukazuje příklad přidání ovládacích prvků data a času do formuláře.

1. Přidejte do formuláře kontroler pro každý ovládací prvek data a času, který by měl formulář obsahovat. (Počet kontrolerů se musí rovnat počtu ovládacích prvků data a času ve formuláři.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Deklarujte požadované proměnné (typu `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Vytvořte metody, kde bude datum a čas aktualizován kontrolery typu datetime. Následující příklad ukazuje jednu takovou metodu.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Nastavte chování každého kontroleru typu datetime a připojte každý kontroler k části formuláře. Následující příklad ukazuje, jak nastavit data pro ovládací prvky datum-počáteční a čas-počáteční. Podobný kód můžete přidat do ovládacích prvků datum-konečný a čas-konečný (nezobrazeno).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Pokud vše, co potřebujete, je ovládací prvek kalendářního data, můžete přeskočit nastavení ovládacího prvku času a místo toho pouze nastavit ovládací prvek data, jak je znázorněno v následujícím příkladu:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Další prostředky

- [Styl rozhraní pro provádění výrobního provozu](production-floor-execution-styles.md)
- [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md)
