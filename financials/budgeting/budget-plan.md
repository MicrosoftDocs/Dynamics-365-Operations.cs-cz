---
title: "Plánování rozpočtu"
description: "Cílem této laboratoře je poskytnout zobrazení Microsoft Dynamics 365 s asistencí pro operace aktualizace funkce v oblasti plánování rozpočtu. Tento seminář ukazuje příklad rychlé konfigurace modulu plánování rozpočtu a znázorňuje, jak lze provést plánování rozpočtu pomocí této konfigurace.  Tuto laboratoř se soustředí zejména na následujících obchodních procesů nebo úloh – vytváření organizační hierarchii rozpočtu, plánování a konfiguraci zabezpečení uživatele - definování scénáře plánu rozpočtu, rozpočtu plán sloupce, rozložení a šablony aplikace Excel - vytvoření a aktivaci rozpočtové plánování procesu - vytváření dokument plánu rozpočtu pomocí vytažení skutečné hodnoty z hlavní knihy - přidělení pomocí upravit data dokumentu plánu rozpočtu - úpravy rozpočtu plán dokumentu data v aplikaci Excel"
author: twheeloc
manager: AnnBe
ms.date: 2015-10-26 03 - 31 - 44
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Plánování rozpočtu

Cílem této laboratoře je poskytnout zobrazení Microsoft Dynamics 365 s asistencí pro operace aktualizace funkce v oblasti plánování rozpočtu. Tento seminář ukazuje příklad rychlé konfigurace modulu plánování rozpočtu a znázorňuje, jak lze provést plánování rozpočtu pomocí této konfigurace.  Tuto laboratoř se soustředí zejména na následujících obchodních procesů nebo úloh – vytváření organizační hierarchii rozpočtu, plánování a konfiguraci zabezpečení uživatele - definování scénáře plánu rozpočtu, rozpočtu plán sloupce, rozložení a šablony aplikace Excel - vytvoření a aktivaci rozpočtové plánování procesu - vytváření dokument plánu rozpočtu pomocí vytažení skutečné hodnoty z hlavní knihy - přidělení pomocí upravit data dokumentu plánu rozpočtu - úpravy rozpočtu plán dokumentu data v aplikaci Excel 

<a name="prerequisites"></a>Předpoklady 
------------------

Pro účely tohoto návodu budete potřebovat 365 Dynamics pro prostředí operací s daty společnosti Contoso demo a zřídit jako správce instance. Nepoužívejte v privátní režim prohlížeče pro tuto laboratoř - odhlásit z jiného účtu v prohlížeči, v případě potřeby a přihlásit pomocí Dynamics 365 pověření správce operace. Při přihlášení do 365 Dynamics pro operace, je **musí**, zaškrtněte políčko "Zachovat me přihlášeni". Tímto krokem zajistíte vytvoření trvalého souboru cookie, který aplikace Excel momentálně vyžaduje. Pokud přihlášení k Dynamics 365 pro operace pomocí prohlížeče než IE, pak budete vyzváni k přihlášení do aplikace Excel. Po kliknutí na tlačítko „Přihlásit” v aplikaci Excel se otevře místní okno IE a při přihlašování **MUSÍTE** zaškrtněte políčko „Zůstat přihlášeni”. Pokud se zdá, že volba „Přihlásit se” v aplikaci Excel nemá žádný účinek, vyprázdněte mezipaměť souborů cookie v IE.

## <a name="scenario-overview"></a>**Scenario overview**
Julie pracuje jako finanční manažerka společnosti Contoso Entertainment Systems v Německu (DEMF). S blížícím se fiskálním rokem 2016 potřebuje pracovat na nastavení rozpočtu společnosti pro nadcházející rok. Příprava rozpočtu vypadá takto:

1.  Julie použije skutečná množství z předchozího roku výchozí bod k vytvoření rozpočtu.
2.  Na základě skutečných hodnot z předchozího roku vytvoří odhady pro 12 měsíců v nadcházejícím roce.
3.  Julie projde rozpočet s finančním ředitelem. Po dokončení provádí nezbytné úpravy plánu rozpočtu a dokončuje přípravu rozpočtu.

Schéma konfigurace scénáře plánování rozpočtu vypadá takto:

![Screenshot1](./media/screenshot1-300x152.png)

Helena následující šablonu aplikace Excel používá při přípravě rozpočtu:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Cvičení 1: Konfigurace
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Úloha 1: Vytvoření organizační hierarchie**
Protože se proces rozpočtování odehrává ve finančním oddělení, Julie potřebuje vytvořit velmi jednoduchou organizační hierarchii tvořenou pouze finančním oddělením. 1.1. Přejděte do organizační hierarchie (Správa organizace &gt;organizace &gt;organizační hierarchie) a klepněte na tlačítko Nový

![Screenshot3](./media/screenshot3.png) 

1.2. Zadejte název organizační hierarchie a klepněte na tlačítko Přiřadit účel

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Vyberte účel plánování rozpočtu, klepněte na tlačítko Přidat a přiřaďte nově vytvořené organizační hierarchie: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Zopakujte krok výše s účelem zabezpečení organizace. Po dokončení formulář zavřete.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Ve formuláři Organizační hierarchie klikněte na tlačítko Zobrazit. Klikněte na tlačítko Upravit v Návrháři hierarchie a vytvořte hierarchii kliknutím na tlačítko Vložit.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Vyberte Finanční oddělení pro hierarchii rozpočtování. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Po dokončení klikněte na tlačítko Publikovat a zavřít. 1/1/2015 vyberte jako datum účinnosti pro publikování hierarchie.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Úkol 2: Konfigurace zabezpečení pro uživatele
Plánování rozpočtu používá zvláštní zásady zabezpečení pro konfiguraci přístupu k datům rozpočtových plánů. Julie musí udělit přístup k finančním plánům rozpočtu sama sobě. 2.1. Přepnutí kontextu právnické osoby DEMF: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Přejít na rozpočtování &gt;nastavení &gt;plánování rozpočtu &gt;konfiguraci plánování rozpočtu. V kartě Parametry hodnota zabezpečení model založený na zabezpečení organizace [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Přejít na stránku Správa systému &gt;uživatele &gt;uživatele. Přiřaďte uživateli Admin (Julii Funderburk) roli správce rozpočtu. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Vyberte roli uživatele a klikněte na položku přiřadit organizace [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Zvolte možnost „Udělit přístup ke specifickým organizacím”. Vyberte organizační hierarchii vytvořenou v prvním kroku. Vyberte uzel Finance a klepněte na tlačítko udělit pomocí tlačítka děti ***důležité!*** *– Přesvědčte se, zda se do kontextu DEMF právnické osobě při provádění tohoto úkolu jako organizační zabezpečení platí za právnickou osobu*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Úkol 3: Vytvoření scénáře
3.1. Přejít na rozpočtování&gt;nastavení &gt;plánování rozpočtu &gt;konfiguraci plánování rozpočtu. Na stránce Scénáře si všimněte scénářů, které budeme později v tomto semináři používat: Skutečné hodnoty předchozího roku a Rozpočtováno *Poznámka: pokud chcete, můžete pro toto cvičení vytvořit a používat nové scénáře.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Poznámka: Helena nepoužívá formálního schvalovacího procesu pro přípravu rozpočtu, přeskočí jsme pracovní postupy, fáze a fáze pracovního postupu instalace této laboratoře a použije existující nastavení pro automatické – schválení pracovního postupu. Viz dodatek k této konfiguraci pracovního postupu.*

## <a name="task-4-create-budget-plan-columns"></a>Úkol 4: Vytvoření sloupců plánu rozpočtu
Sloupce plánu rozpočtu jsou buď peněžní, nebo množstevní sloupce, které lze použít v rozvržení dokumentu plánu rozpočtu. V našem příkladu je nutné vytvořit sloupec pro skutečné hodnoty předchozího roku a 12 sloupců představujících každý měsíc rozpočtu předchozího roku. Sloupce lze vytvářet buď kliknutím na tlačítko Přidat a zadáním hodnot, nebo využitím datové entity. V tomto semináři použijeme datovou entitu k vyplnění hodnot. 4.1. V modulu rozpočtování&gt;nastavení &gt;plánování rozpočtu &gt;rozpočtové plánování konfigurace otevřené sloupců stránky. Klepněte na tlačítko Office v pravém horním rohu formuláře a vyberte sloupce (nefiltrovaný) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Systém otevře sešit aplikace Excel pro vyplnění hodnot. Pokud budete vyzváni, klepněte na tlačítko Povolit úpravy a důvěřovat této app [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Potřebujeme k vyplnění hodnot více sloupců. Klepněte na pravé straně podokna přidat sloupce do mřížky návrhu: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Klepněte na tlačítko malá tužka vedle PlanColumns Chcete-li zobrazit dostupné sloupce do mřížky přidat [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Poklepejte na každé pole přidat do vybraná pole a klepněte na tlačítko Aktualizovat [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Do tabulky aplikace Excel přidejte všechny sloupců, které je třeba vytvořit. Použijte funkci automatického vyplňování v aplikaci Excel pro rychlé přidání řádků. Přesvědčte se, zda jsou přidány řádky v rámci tabulky (používáte-li svislý posuvník, je třeba zobrazit záhlaví sloupců v horní části mřížky) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Vraťte se do 365 Dynamics pro operace a aktualizujte stránku. Publikované hodnoty budou zobrazeny ve 365 Dynamics pro operace. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Úkol 5: Vytváření rozvržení dokumentu plánu rozpočtu a šablon
Rozvržení definuje, jakým způsobem bude mřížka řádků dokumentu plánu rozpočtu vypadat, až uživatel otevře dokument plánu rozpočtu. Dále je možné přepnout rozvržení dokumentu plánu rozpočtu, aby se zobrazila stejná data v různých úhlech. Protože Julie definovala sloupce pro použití s dokumentem plánu rozpočtu, potřebuje nyní vytvořit rozvržení dokumentu plánu rozpočtu, které bude vypadat podobně jako tabulka aplikace Excel, kterou používá k vytvoření dat rozpočtu (viz část Přehled scénáře v tomto semináři) 5.1. V modulu rozpočtování&gt;nastavení &gt;plánování rozpočtu &gt;rozpočtové plánování konfigurace otevřít rozložení stránky. Vytvořte nové rozvržení pro měsíční položku rozpočtu:

-   Vyberte sadu dimenzí MA+BU, abyste zahrnuli hlavní účty a obchodní jednotky do rozvržení.
-   Uveďte všechny sloupce plánu rozpočtu vytvořené v předchozím kroku v oddílu Prvky. Povolte úpravy u všech položek s výjimkou skutečných hodnot z předchozího roku.
-   Kliknutím na tlačítko Popisy vyberte finanční dimenze, které mají zobrazit popisy v mřížce.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) podle rozpočtu plánu můžete vytvořit šablony aplikace Excel, který má být použit jako alternativní způsob úpravy dat rozpočtu definice rozložení. Protože se šablona aplikace Excel musí shodovat s definicí rozložení plánu rozpočtu, nebude možné upravit rozložení plánu rozpočtu po generování šablony aplikace Excel. Proto tento úkol proveďte až po definování všech komponentů rozvržení. 5.2. Pro rozvržení vytvořených 5.1. Krok, klepněte na tlačítko šablony &gt;generovat. Potvrďte varovnou zprávu. Chcete-li zobrazit šablony, klepněte na položku Šablona &gt;zobrazení. *Poznámka: Ujistěte se, vyberte "Uložit jako" a vyberte umístění, do které chcete šablonu uložit ji chcete upravit. Pokud uživatel vybere v dialogovém okně bez uložení "Otevřené", nebudou změny provedené v souboru zachovány při zavření souboru.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Volitelný krok&gt; šablona aplikace Excel upravit aby vypadaly více uživatel popisný – Přidání celkového vzorce polí záhlaví, formátování atd. Uložte změny a uložte soubor do rozpočtu plán rozložení klepnutím rozložení &gt;odeslat [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Úkol 6: Vytvoření procesu plánování rozpočtu
Julie potřebuje vytvořit a aktivovat nový procesu plánování rozpočtu spojením celého nastavení uvedeného výše, aby mohla začít zadávat plány rozpočtu. Proces plánování rozpočtu definuje, které rozpočtovací organizace workflow, rozvržení a šablony se použijí pro vytváření plánů rozpočtu. 6.1. Přejít na rozpočtování &gt;nastavení &gt;plánování rozpočtu &gt;procesu plánování rozpočtu a vytvořit nový záznam.

-   Proces plánování rozpočtu – rozpočtování DEMF pro fiskální rok 2016
-   Rozpočtový cyklus – fiskální rok 2016
-   Hlavní kniha – DEMF
-   Výchozí účetní struktura – výroba zisků a ztrát
-   Organizační hierarchie – vyberte hierarchii vytvořenou na začátku semináře
-   Workflow plánování rozpočtu – přiřaďte Automatickém schválení workflow pro finanční oddělení
-   V pravidlech fází plánování rozpočtu a šablon u všech workflowů fáze plánování rozpočtu vyberte, jestli jsou přidávání řádků a úpravy řádků povolené a jaké rozvržení se má použít jako výchozí

*Poznámka: Můžete vytvořit další rozvržení dokumentu a zpřístupnit je ve fázi workflowu plánování rozpočtu kliknutím na tlačítko Alternativní rozložení.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Vyberte akce &gt;aktivace aktivovat workflow plánování rozpočtu [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Cvičení 2: Simulace procesu
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Úkol 7: Generování počátečních dat pro plán rozpočtu z hlavní knihy
7.1. Přejít na rozpočtování &gt;periodické &gt;Generovat plán rozpočtu z hlavní knihy. Zadejte parametry periodického procesu a klikněte na tlačítko Generovat. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Přejít na rozpočtování &gt;plánů rozpočtu k nalezení vytvořené procesu Generovat plán rozpočtu. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Otevřete podrobnosti dokumentu kliknutím na odkaz Číslo dokladu. Plán rozpočtu je zobrazen podle rozložení vytvořen během této laboratoře [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Úkol 8: Vytvoření rozpočtu pro aktuální rok podle skutečných hodnot předchozího roku
Metody přidělení lze použít v plánu rozpočtu ke snadnému kopírování informací pro plány rozpočtu z jednoho scénáře do jiného / jejich rozdělení do období / přidělení k dimenzím. Použijeme přidělení k vytvoření rozpočtu pro aktuální rok ze skutečných hodnot předchozího roku. 8.1. Vybrat všechny řádky v mřížce dokumentu plánu rozpočtu a klepněte na tlačítko přidělit rozpočet [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Vyberte metodu přidělení, klíč období, zdrojové a cílové scénáře a klepnutím na tlačítko přidělit 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Předchozí rok skutečných částek, které budou zkopírovány do rozpočtu na běžný rok a přidělit napříč obdobími pomocí klíče období prodeje křivka. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Úkol 9: Úprava dokumentu plánu rozpočtu pomocí aplikace Excel a dokončení dokumentu
9.1. Klepněte na tlačítko list otevřete obsah dokumentu v aplikaci Excel

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Po otevření sešitu aplikace Excel upravte čísla v dokumentu plánu rozpočtu a klikněte na tlačítko Publikovat.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Vrátit dokument plánu rozpočtu v 365 Dynamics pro operace. Klepněte na tlačítko pracovní postup &gt;odeslat automatické schvalování dokumentu

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Po dokončení pracovního postupu dokumentu fázi plánu rozpočtu změní na Schváleno. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Dodatek
========

### <a name="auto-approve-workflow-configuration"></a>Konfigurace automatického schválení workflow

A. Rozpočet &gt;nastavení &gt;plánování rozpočtu &gt;workflowy rozpočtování vytvořit nový pracovní postup pomocí šablony workflowy plánování rozpočtu:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Tento pracovní postup bude obsahovat pouze jeden úkol – Přechod fáze plánu rozpočtu 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Uložte a aktivujte pracovní postup. 

B. Přejít na rozpočtování &gt;nastavení &gt;plánování rozpočtu &gt;konfiguraci plánování rozpočtu. Postupně vytvořit kartu 2 fáze – počáteční a odesláno 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Přejít na rozpočtování &gt;nastavení &gt;plánování rozpočtu &gt;konfiguraci plánování rozpočtu. V dílčí fáze pracovního postupu na kartě přidružení pracovního postupu automaticky – schválit vytvořili v kroku s fázemi počáteční a odesláno 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


