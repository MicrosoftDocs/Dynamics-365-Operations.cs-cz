---
title: Architektura průvodce procesem
description: Toto téma poskytuje informace o rámci průvodce procesem pro vývojáře, kteří rozšiřují naše skladové mobilní procesy v X++.
author: MarkusFogelberg
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: ecf4bf884bca80cabb066ae43d38cd9c0e159216
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651949"
---
# <a name="process-guide-framework"></a>Architektura průvodce procesem

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o rámci průvodce procesem pro vývojáře, kteří rozšiřují naše skladové mobilní procesy v X++. Mobilní procesy skladu jsou rozšiřitelné díky rozdělení procesů na malé kroky. Budování obchodní logiky a uživatelského rozhraní každého kroku bylo extrahováno do jednotlivých tříd, což umožňuje rozšiřitelnost.

## <a name="overview-of-the-existing-design"></a>Přehled stávajícího návrhu

Mobilní toky provádění skladu jsou vystaveny prostřednictvím jediného koncového bodu vlastní služby. Požadavek přichází z mobilní aplikace ve formě řetězce XML, který obsahuje metadata uživatelského rozhraní prezentovaného v mobilní aplikaci a také hodnoty zadané uživatelem.

Když je požadavek přijat, prvním krokem je deserializace tohoto XML. Třída **WHSMobileAppServiceXMLTranslator** převede XML na kontejner, který obsahuje jak řídicí informace, tak informace o relaci.

Poté se informace v kontejneru použijí k odvození, na kterém skladovém procesu uživatel pracuje nebo se chystá začít (reprezentováno výčtem **WHSWorkExecuteMode**), a podle toho vytvořit instanci odvozené třídy **WHSWorkExecuteDisplay**. Je vyvolána metoda **displayform()**, která pak provede následující:

-   Zpracovává údaje od uživatele (delegované na třídu **WHSRFControlData**, ale některé procesy implementují specifickou logiku přepsáním metody **processControl()**).

-   Vykoná obchodní logiku.

-   Zvýší krok.

-   Sestaví kontejner představující nové uživatelské rozhraní (obvykle v metodě **build…()**).

Kontejner je poté vrácen překladači, který pak serializuje XML a odešle ho zpět jako odpověď do mobilního zařízení.

Následující schéma postupu přehledně znázorňuje přehled tok spuštění. Všimněte si, že diagram je spíše schematickým přehledem a není znázorněním skutečného kódu v poměru 1:1.

![Schématický přehled procesu.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Důvod změny designu

Výše uvedený návrh nabízí velmi jednoduchý rámec pro budování procesů používaných v mobilních tocích. Jak je však patrné výše, metody **displayform()** přebírají více odpovědností. Deleguje je na jiné metody a třídy, ale při absenci konkrétních odpovědností za třídu se to děje napříč třídami nekonzistentním způsobem. Vzhledem k tomu, že počet podporovaných scénářů organicky roste, některé z těchto tříd se mohou stát poměrně složitými. Aby to bylo zajímavější, některé z těchto tříd/metod jsou přepsány a znovu použity ve více režimech. Výsledkem jsou extrémně dlouhé metody s vysokou cyklomatickou složitostí. Ty v minulosti představovaly problémy s údržbou. Oprava chyb v těchto metodách byla riskantní a náchylná k regresi.
Například, metoda **processWorkLine()** v třídě **WhsWorkExecuteDisplay** je odkazována z více procesů (v podstatě kdekoli, kde se provádí práce).

Aby byly tyto rozšiřitelné, jednou z možností by bylo rozdělení metod **displayForm** do menších metod a zavést body rozšiřitelnosti. Kvůli matici scénářů by však pro partnery bylo náročné psát rozšíření a ověřovat je proti regresím. Nejen to, kvůli výše uvedenému nedostatku strukturovaného rozdělení odpovědnosti by se kód v průběhu času neustále rozrůstal nepředvídatelným způsobem, což by představovalo problémy při vytváření kvalitních rozšíření.

V důsledku toho je přepracování udržitelnou možností s cílem mít jasně definované třídy s nezávislými odpovědnostmi. Třída by měla mít jednu odpovědnost, jeden důvod ke změně a jeden důvod k rozšíření.

## <a name="design-overview"></a>Přehled designu

V přepracovaném rámci se základní strategie točí kolem dvou principů: rozdělit tok provádění na jednotlivé komponenty s dobře definovanými odpovědnostmi a mít dobře definované body rozšíření v každé z komponent.

Název nového rámce je „ProcessGuide“. Důvodem je, že cílem těchto tříd je provést uživatele obchodním procesem (na rozdíl od bohatého klienta, což je prostředí založené na formulářích, kde má uživatel větší flexibilitu v tom, jak interaguje s daty nebo v jakém pořadí provádí úkoly).

> [!NOTE]
> Jedním z pozoruhodných detailů je záměrné vynechání předpony „WHS“. Zatímco mobilní procesy byly původně zavedeny pro skladování, následně překročily hranice a podporovaly různé procesy výroby a řízení zásob. V důsledku toho byla v názvu rámce vyloučena reference na sklad.

Chcete-li identifikovat komponenty, prvním krokem je podívat se na proces zahájení výroby (třída **WhsWorkExecuteDisplayProdStart**). Zde je schéma procesu.

![Obrázek schematického procesu.](media/production-start-process-schematic.png)

Podíváme-li se na tok řízení, jsou potřeba následující komponenty:

-   Řadič, který propojí celý obchodní proces.
-   Krok zodpovědný za provedení kroku v procesu.
-   Zpracovatel dat pro zpracování dat v kroku.
-   Tvůrce stránek odpovědný za vytvoření uživatelského rozhraní pro krok.
-   Navigační agent zodpovědný za krokový přechod.
-   Třída zodpovědná za provádění obchodního procesu.

Pokud ve výše uvedeném vývojovém diagramu procesu začnete krokem 1 a začnete zpracovávat data z předchozího kroku, a poté skončíte vytvořením uživatelského rozhraní, budou data pokračovat ve zpracování v dalším kroku. To zavádí těsné spojení mezi po sobě jdoucími kroky, v důsledku čehož by naše nové schéma na vysoké úrovni vypadalo takto:

![Obrázek schématického procesu na vysoké úrovni.](media/high-level-schematic.png)

Níže jsou uvedeny klíčové součásti přepracovaného procesu:

-   **ProcessGuideController** – Tato třída řídí celkové provádění obchodního procesu. Definuje továrny, které vytvářejí instanci kroku a navigačního agenta, který následně tvoří provádění procesu, a také logiku čištění pro zrušení nebo ukončení procesu.

-   **ProcessGuideStep** – Tato třída představuje jeden jediný krok v obchodním procesu. Tato třída obsahuje definici továren, které vytvářejí instanci tvůrce stránek, akcí a datových procesorů a je zodpovědná za jejich vyvolání ve správném pořadí.

-   **ProcessGuideNavigationAgent** – Tato třída je zodpovědná za navigaci mezi kroky. Po dokončení kroku je navigační agent zodpovědný za definování dalšího kroku a předá všechny parametry, které může předchozí krok vyžadovat, aby sdělil následující.

-   **ProcessGuidePageBuilder** – Tato třída je zodpovědná za vytvoření instance uživatelského rozhraní.

-   **ProcessGuideAction** – Tato třída představuje akci, která se uživateli zobrazuje jako tlačítko.

-   **ProcessGuideDataProcessor** – Tato třída je zodpovědná za zpracování dat zadaných uživatelem do pole.

## <a name="execution-flow"></a>Průběh provádění

Počáteční bod toku provádění zůstává nezměněn. Požadavek tedy stále přichází přes stejné koncové body, po kterém následuje deserializace XML do kontejneru. Tento kontejner je poté předán do **getNextFormState()**.

Je třeba poznamenat tři důležité třídy:

-  **ProcessGuideSessionState** – Obsahuje informace o stavu relace – režim, průchod, kontroler a prováděný krok a tak dále.

-  **ProcessGuidePage** – Obsahuje silně typovanou reprezentaci metadat uživatelského rozhraní.

-  **ProcessGuideRequest** – Obsahuje dva výše uvedené členy a jedná se o silně typovanou reprezentaci požadavku přijatého z mobilního zařízení.

Tyto třídy jsou vytvořeny pomocí informací o kontejneru (jak stavových, tak uživatelských řídicích dat). Poskytuje typově bezpečný způsob přístupu k hodnotám a manipulaci s nimi. Ve srovnání s opakovaným přístupem ke kontejneru během procesu to přináší výhody jak z hlediska čitelnosti, tak z hlediska výkonu.

Informace o stavu relace se používá k vytvoření instance správné třídy **ProcessGuideController**. Jakmile je vytvořena instance, je vyvolána metoda **createResponse()** v třídě **ProcessGuideController**. Tato metoda je vstupním bodem do logiky procesního průvodce a po provedení se vrací s odpovědí (reprezentovanou v třídě **ProcessGuideResponse**). Odpověď je poté převedena zpět do kontejneru a předána zpět starší logice, která ji poté serializuje do XML a odešle odpověď zpět do mobilního zařízení.

Dále musí ovladač najít další krok, který má provést. Pokud se jedná o začátek nového procesu, regulátor zavolá **initialStep()** k získání prvního kroku v procesu. Poté zavolá metodu **execute()** v **ProcessGuideStep**. Tato metoda vytvoří instanci třídy **ProcessGuidePageBuilder** a zavolá **buildPage()**, který vrátí objekt **ProcessGuidePage**, který je virtuální reprezentací uživatelského rozhraní, které má být prezentováno uživateli. Krok pak pošle výsledek zpět kontroleru, který by pak uloží aktuální stav relace a pak vrátí výsledek zpět do **getNextFormState()** ve formě třídy **ProcessGuideResponse**. Poté je odpověď převedena zpět do kontejneru a následně serializována do XML a odeslána zpět do mobilního zařízení.

Následující sekvenční diagram vysvětluje tento řídicí tok. Všimněte si, že toto je nejběžnější řídicí tok, zjednodušený pro vysvětlení návrhu.

![Zjednodušený tok řízení.](media/control-flow.png)

Když uživatel provede akci na mobilním zařízení kliknutím na tlačítko (nebo naskenováním hodnoty – což obvykle spustí výchozí akci) – požadavek dorazí na metodu **createResponse()** v třídě **ProcessGuideController** stejnou cestou. Tentokrát však kontroler z informace o stavu relace ví, ve kterém kroku se uživatel nachází. V souladu s tím vytvoří instanci vhodné třídy **ProcessGuideStep** a vyvolá metodu execute. **ProcessGuideStep** zase přečte název akce vyvolaný uživatelem a poté vytvoří příslušnou instanci třídy **ProcessGuideAction** a zavolá **execute()**.

Třída **ProcessGuideAction** je zodpovědná za provedení konkrétní akce, existují však dvě významné výjimky.

První z nich je třída **ProcessGuideOKAction**. Tato akce znamená, že uživatel chce proces potvrdit a posunout se vpřed. V souladu s tím – tato metoda ve skutečnosti provede zpětné volání třídy ProcessGuideStep, což znamená, že krok vyvolá **processData()** v **ProcessGuideDataProcessor**. Tím se zpracují data, která uživatel zadal, a poté se aktualizuje stav kroku a výsledek se odešle zpět kontroleru. V závislosti na výsledku procesoru krok vyvolá tvůrce stránek k vytvoření příslušného uživatelského rozhraní nebo nastaví stav kroku jako dokončený. To se odráží v horní polovině níže uvedeného sekvenčního diagramu.

Další výjimkou je akce zrušení, implementovaná v třídách **ProcessGuideCancelResetProcessAction** a **ProcessGuideCancelExitProcessAction**. Tyto akce představují záměr zrušit proces a vrátit se buď na začátek procesu, nebo proces úplně ukončit. Podobné jako akce **OK** tyto akce také provedou zpětné volání kroku, které signalizuje záměr do **ProcessGuideController**. Kontroler pak provede nezbytné vyčištění stavových proměnných a buď přesune řízení do počátečního kroku v procesu, nebo proces úplně ukončí.

Po dokončení kroku, pokud je stav kroku nastaven na **Dokončeno**, pak ovladač vytvoří instanci **ProcessGuideNavigationAgent**, která vrátí název dalšího kroku. Kontroler pak vytvoří instanci tohoto kroku a vyvolá metodu **execute()** metoda – a cyklus pokračuje. Nejčastěji nový krok vyvolá odpovídající **ProcessGuidePageBuilder** k vytvoření uživatelského rozhraní pro další obrazovku, která má být prezentována uživateli a která je poté odeslána zpět. Tento tok se vyobrazen v dolní polovině níže uvedeného sekvenčního diagramu.

![sekvenční diagram.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Vytváření nového procesu pomocí frameworku ProcessGuide

Nejlepší způsob, jak vysvětlit tok řízení, je použít příklad, který existuje v aplikaci – proces spuštění výroby.

## <a name="overview-of-the-production-start-process"></a>Přehled spuštění procesu výroby

Začněme pochopením toku procesu. V prvním kroku je uživatel vyzván k zadání ID výrobní zakázky.

![Výzva na ID produkce.](media/production-id-prompt.png)

Když uživatel zadá ID výrobní zakázky, ověří se číslo objednávky. Některá spouštěná ověření jsou založena na tom, zda je objednávka ve stejném skladu, do kterého je uživatel přihlášen, a na stavu objednávky. Pokud se ověření nezdaří, uživateli se zobrazí chybová zpráva. Pokud je ověření úspěšné, zobrazí se uživateli podrobnosti o výrobní zakázce a položce.

Uživatel může buď zrušit a vrátit se na začátek procesu, nebo kliknout **OK** pro potvrzení. V druhém případě je výrobní zakázka nastavena na stav **Zahájeno**, jsou zaúčtovány odpovídající deníky, ovládání se vrátí zpět k prvnímu kroku a uživateli se zobrazí zpráva „Práce dokončena“.


## <a name="creating-the-controller"></a>Vytvoření kontroleru

Prvním krokem při budování obchodního procesu je vytvoření třídy řadiče, která se rozšiřuje z abstraktní třídy **ProcessGuideController**, která implementuje výchozí chování ovladače. Nový název třídy je **ProdProcessGuideProductionStartController** a obohacený o hodnotu **WHSWorkExecuteMode** **StartProdOrder**. Používá se stejné vytvoření instance na základě **SysExtension**, které bylo použita v třídách **WHSWorkExecuteDisplay**, což pomáhá vytvořit instanci ovladače, když uživatel provede položku nabídky pro tento režim.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Vzor pojmenování třídy je **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Toto je vzor, který se používá pro třídy řadičů a rozšiřuje se na další třídy.


## <a name="building-the-first-step"></a>Vytvoření prvního kroku

Dále k definici prvního kroku vytvoříte třídu **ProdProcessGuidePromptProductionIdStep** rozšiřující se z **ProcessGuideStep**.

Úkol vytvoření instance třídy je delegován na továrnu kroků, kterou vyvolá základní třída **ProcessGuideController**. Výchozí implementace továrny vytvoří instanci kroku na základě názvu. Proto k vytvoření instance **ProdProcessGuidePromptProductionIdStep** jako prvního kroku v ovladači musíte udělat dvě věci:

-   Přidat k třídě **ProdProcessGuidePromptProductionIdStep** atribut **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Ve třídě kontroleru implementujte abstraktní metodu **initialStepName()** k vrácení názvu kroku.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Hodnota v atributu **ProcessGuideStepName** nemusí přesně odpovídat názvu třídy, jak je uvedeno výše. Implementace toho však umožňuje jednotnost a typovou bezpečnost kolem křížových odkazů při použití třídy. Použití této konvence pojmenování se doporučuje.
>
> Vytvoření instance na základě **ProcessGuideStepName** je implementováno v třídě **ProcessGuideStepDefaultFactory**. Ve vzácných případech, kdy chcete jinou strategii pro vytvoření instance kroku, musíte provést následující:
> -   Vytvořte novou tovární třídu dědění z **ProcessGuidStepAbstractFactory**.
> -   Volitelně vytvořte novou třídu parametrů implementující rozhraní **ProcessGuideIStepCreationParameters**, obsahující parametry, které by továrna potřebovala.
> -   Ve své třídě ovladačů přepište **stepFactory()** a metody **stepCreationParameters()** pro vrácení výše uvedených továren a parametrů.

Dalším krokem je implementace funkčnosti třídy **ProdProcessGuidePromptProductionIdStep**. Musíte implementovat logiku pro vytváření uživatelského rozhraní, zpracování dat zadaných uživatelem a určení, kdy je krok dokončen.

### <a name="building-the-user-interface-for-the-first-step"></a>Vytvoření uživatelského rozhraní pro první krok

Uživatelské rozhraní je vytvořeno pomocí třídy zděděné z abstraktní třídy **ProcessGuidePageBuilder**. Pro tento krok pojmenujte třídu, aby reprezentovala, co dělá – **ProdProcessGuidePromptProductionIdPageBuilder**.

Mechanismus vytváření instance třídy je podobný tomu, jak byl krok vytvořen z kontroleru. 

-   Přidejte k třídě **ProdProcessGuidePromptProductionIdPageBuilder** atribut **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   V třídě **ProdProcessGuidePromptProductionIdStep** implementujte abstraktní metodu **pageBuilderName()**, aby se vrátil tento název.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Podobně jako u továrny kroků je zde také implementován abstraktní tovární vzor pro továrnu na tvorbu stránek. Ve vzácných případech, kdy chcete jinou strategii pro vytvoření instance tvůrce stránek, tedy můžete provést následující:
> - Vytvořte novou tovární třídu dědící z **ProcessGuidePageBuilderAbstractFactory**.
> - Volitelně vytvořte novou třídu parametrů implementující rozhraní **ProcessGuideIPageBuilderCreationParameters**, obsahující parametry, které by továrna potřebovala.
> - Ve své třídě kroků přepište **pageBuilderFactory()** a metody **pageBuilderCreationParameters()** pro vrácení výše uvedených továren a parametrů.

K implementaci uživatelského rozhraní potřebujete stránku s jedním textovým polem pro zadání ID výrobní zakázky a navíc tlačítka **OK** a **Zrušit**. Tlačítko **Zrušit** by mělo ukončit proces.

Chcete-li to implementovat, musíte přepsat dvě metody v třídě **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Použijte metodu **addDataControls()** k přidání textového pole.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Použijte metodu **addActionControls()** k přidání tlačítek **OK** a **Zrušit**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Tím se přidají ovládací prvky dat, následované tlačítky. Pokud však chcete vytvořit obrazovku s rozptýlenými ovládacími prvky dat a tlačítky, můžete místo toho přepsat metodu **addControls()** pro flexibilitu.

Další scénář, který je třeba zvážit, je, jak znovu sestavit stránku v případě selhání ověření, například pokud uživatel zadá nesprávné ID výrobní zakázky. Základní třída **ProcessGuidePageBuilder** implementuje výchozí chování, které znovu sestaví uživatelské rozhraní, vymaže naskenovanou hodnotu a přidá kontrolu chyb s chybovou zprávou. Protože se jedná o výchozí chování, které chcete použít, nemusíte přidávat žádný kód pro zpracování chyb.

> [!TIP]
> Pokud chcete implementovat vlastní chování uživatelského rozhraní pro chybové situace, můžete přepsat jednu nebo více metod **rebuildFromRequestPage()**, **isErrorState()** a **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Zpracování uživatelem zadaných údajů v prvním kroku

Zpracování dat se provádí v třídě **ProcessGuideDataProcessorDefault**, která se zase vyvolává starší třídu **WhsRfControlData**. V tomto výchozím chování nejsou potřeba žádné změny a **WhsRfControlData** již má logiku pro ověření pole **ProdId**, takže pro manipulaci s tímto nemusíte psát žádnou logiku. V případě požadovaných rozšíření pro ověřovací logiku zvažte použití mechanismu rozšíření na základě **WhsControl**.

### <a name="determine-if-the-first-step-is-complete"></a>Zjistěte, zda je první krok dokončen

Když je ověření úspěšné, je čas označit krok jako dokončený. To se provádí v základní třídě, ale musíte implementovat podmínku, abyste určili dokončení kroku. K tomu slouží následující přepsaná metoda.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Krok 2: Zobrazte podrobnosti objednávky a potvrďte

Ve druhém kroku procesu se uživateli zobrazí obrazovka s podrobnostmi o objednávce. Uživatel může buď kliknout na tlačítko **OK** pro potvrzení zahájení výrobní zakázky nebo kliknout na **Zrušit** pro návrat na začátek procesu. V tomto příkladu pojmenujte krok **ProdProcessGuideConfirmProductionOrderStep** a třídu pro tvorbu stránek **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Třída ProdProcessGuideConfirmProductionOrderStep vypadá následovně.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Protože zde uživatel nezadává žádné hodnoty, nemusíte přepisovat metodu **isComplete()**. Krok je dokončen, když uživatel klikne na **OK**.

Třída Tvůrce stránek přepíše metodu **addDataControls()** pro přidání tří štítků. První štítek zobrazuje ID výrobní zakázky, druhý obsahuje informace o položce (jako je ID položky, rozměry nebo popis) a třetí obsahuje množství a měrnou jednotku.

**addActionControls()** je pak přepsáno přidáním 2 tlačítek – tlačítka **OK** a tlačítka **Zrušit** tlačítko pro zrušení procesu a návrat na začátek procesu.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Stejný zdrojový kód pro metody X++ v tomto tématu můžete najít pomocí Průzkumníka aplikací. Filtrujte název třídy a poté klikněte pravým tlačítkem na název třídy a vyberte **Zobrazit kód**.

### <a name="step-3-start-the-production-order"></a>Krok 3: Spuštění výrobní zakázky

Třetím krokem je provedení obchodní logiky zahájení výrobní zakázky. Tento krok se poněkud liší od předchozích kroků v tom, že tento krok nemá uživatelské rozhraní. Tento krok se provede tiše, když uživatel klikne na **OK** v předchozím kroku.

Abstraktní třída **ProcessGuideStepWithoutPrompt** implementuje výchozí chování pro takové kroky. Současný krok by proto měl rozšířit třídu **ProcessGuideStepWithoutPrompt** a přepsat metodu **doExecute()**.

Následující příklad kódu ukazuje třídu a implementaci metody **doExecute()**. Metoda jednoduše načte ID objednávky a ID uživatele ze stavu relace a vyvolá metodu ke spuštění této výrobní zakázky.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

V případě výjimky logika zpracování výjimek frameworku zajistí, že se proces vrátí zpět k předchozímu kroku.

> [!NOTE]
> Vyvolání **addProcessCompletionMessage()** přidá k parametrům navigace zprávu „Práce dokončena“. V dalším kroku (za předpokladu, že má uživatelské rozhraní) se zobrazí tato zpráva. Základní třídy zpracovávají tuto logiku a k dosažení tohoto chování není třeba přidávat do tříd procesů žádný specifický kód.


### <a name="building-the-navigation-through-the-steps"></a>Sestavení navigace pomocí kroků

Základní třída **ProcessGuideController** vytváří instanci třídy **ProcessGuideNavigationAgentDefault**, která se opírá o předem definovanou navigační trasu, což je jednoduchá mapa zdrojových a cílových kroků. Pro scénář zahájení výroby, protože neexistuje žádné podmíněné větvení, by tato implementace postačovala. Proto stačí přepsat metodu **initializeNavigationRoute()** k definování navigační trasy.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Jsou procesy, kde bude docházet k podmíněnému větvení (na základě akcí uživatele, nebo jakýchkoli jiných podmínek). Takové procesy musí dělat následující:

-   Implementujte specifické navigační agenty zděděné z třídy **ProcessGuideNavigationAgent**.

-   Implementujte konkrétní továrnu navigačního agenta zděděnou z třídy **ProcessGuideNavigationAgentAbstractFactory** obsahující logiku pro vytvoření instance správného navigačního agenta na základě aktuálního kroku, stavu relace, akce uživatele nebo jiné logiky.

-   Volitelně přepište **navigationAgentCreationParameters()** ve třídě kontroleru a předat vhodné parametry.

-   Přepište **navigationAgentFactory()** v kontroleru pro vytvoření instance továrny navigačního agenta vytvořené výše.

### <a name="action-classes"></a>Třídy akcí

Třídy akcí představují akce uživatele, takže tento příklad používá akci **OK**, která ukazuje, jak jsou akce vytvořeny.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Třída musí implementovat dvě abstraktní metody:

-   **label()**, která vrátí popisek, který se má zobrazit v ovládacím prvku tlačítka spojeném s touto akcí.

-   **doExecute()**, který akci provede. Jak již bylo zmíněno dříve, tlačítko **OK** jednoduše provede zpětné volání ke kroku. Jiné akce zde však mohou mít složitější logiku.

Akce se konkretizují pomocí rámce **SysExtension** založeného na atributu **ProcessGuideActionName**. Podobně jako při vytváření instancí tvůrců stránek i třída krok implementuje výchozí továrnu akcí a je možné ji přepsat. Tvůrce stránek přidává ovládací prvek tlačítka, jako je tento.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Přitom požádá krok o vytvoření třídy akce pro předané jméno a připojí tuto akci k tlačítku.

### <a name="summary"></a>Souhrn

Abychom shrnuli vše, co bylo v tomto tématu vysvětleno, zde je komplexní shrnutí kódu potřebného pro tento proces:

1.  **ProdProcessGuideProductionStartController**

    1.  Přepište **initialStepName()** k zadání názvu prvního kroku.
    2.  Přepište **initializeNavigationRoute()** k sestavení navigační mapy.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Přepište **isComplete()** k určení, kdy je krok považován za dokončený.
    2.  Přepište **pageBuilderName()** k určení tvůrce stránek, který se má použít.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Přepište **addDataControls()** k přidání textového pole **ID produktu**.
    2.  Přepište **addActionControls()** k přidání tlačítek **OK** a **Zrušit**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Přepište **pageBuilderName()** k určení tvůrce stránek, který se má použít.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Přepište **addDataControls()** k přidání štítků s informacemi o objednávce, položce a množství.

    2.  Přepište **addActionControls()** k přidání tlačítek **OK** a **Zrušit**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Metoda **createItemInfoForProdId()**, která se používá pro generování informačních štítků položky, je z tohoto tématu vyloučena. Tato metoda se dotazuje na několik tabulek, aby získala ID položky, popis a rozměry. Pokud chcete lépe porozumět **createItemInfoForProdId()**, podívejte se na zdrojový kód.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Přepište **doExecute()** k provedení procesu zahájení výroby a přidání zprávy o dokončení procesu.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Všimněte si, že mnoho běžných vzorů (regenerace uživatelského rozhraní při chybě, zpráva o dokončení procesu nastavení, chování **OK** a **Zrušit**) byly přesunuty do rámce – čímž se vývojáři aplikace ušetří od psaní standardního kódu, který je náchylný k chybám a má riziko nekonzistentního chování napříč procesy. Pokud se však scénář potřebuje odchýlit od běžné cesty, vývojář aplikace má možnost přepsat vhodné metody – ale pak jde o záměrnou odchylku, která je jak explicitní, tak sledovatelná.


### <a name="extending-a-business-process"></a>Rozšíření obchodního procesu

Toto téma dosud zdůrazňovalo, jak vytvořit nový proces pomocí rámce **ProcessGuide**. V této závěrečné části najdete několik příkladů, jak lze tento obchodní proces rozšířit.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Přidání kroku do toku (pomocí ProcessGuideNavigationAgentDefault)

Kam rozšířit:

-   Podřízený třídy **ProcessGuideController** pro proces.

Jak rozšířit:

-   Rozšiřte metodu **initializeNavigationRoute()** ve třídě kontroleru a vyvolejte **addFollowingStep()** v třídě **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Přidání kroku do toku (pomocí vlastního navigačního agenta)

Kam rozšířit:

-   Podřízený z **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Jak rozšířit:

-   Vytvořte novou podřízenou třídu **ProcessGuideNavigationAgent**, která vrátí název požadovaného kroku.

-   Vytvořte novou třídu odvozenou z **ProcessGuideNavigationAgentFactory** která podmíněně vrátí navigačního agenta vytvořeného výše.

-   Rozšiřte metodu **navigationAgentFactory()** v třídě kontroleru pro vrácení továrny vytvořené výše.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Přidejte nový ovládací prvek do uživatelského rozhraní existujícího kroku 

Kam rozšířit:

-   Podřízený z **ProdProcessGuidePageBuilder** pro krok.

Jak rozšířit:

-   Rozšiřte metodu **addDataControls()** a přidejte další kontrolu.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Kompletní přepracování uživatelského rozhraní ve stávajícím kroku

Kam rozšířit:

-   Podřízený z **ProdProcessGuideStep**.

Jak rozšířit:

-   Vytvořte novou podřízenou třídu třídy **ProdProcessGuidePageBuilder** a implementujte požadované uživatelské rozhraní.

-   Rozšiřte metodu **pageBuildeName()** ve třídě kroku k vrácení **ProcessGuidePageBuilderNameAttribute** pro třídu vytvořenou výše.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Změňte logiku, když je krok považován za dokončený

Kam rozšířit:

-   Podřízený z **ProdProcessGuideStep**.

Jak rozšířit:

-   Rozšiřte metodu **isComplete()** k vybudování další logiky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]