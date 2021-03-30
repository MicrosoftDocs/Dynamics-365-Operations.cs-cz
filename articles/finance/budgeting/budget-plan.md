---
title: Plánování rozpočtu
description: Cílem tohoto semináře je poskytnout přehled aktualizací funkcí aplikace Microsoft Dynamics 365 Finance v oblasti Plánování rozpočtu. Tento seminář ukazuje příklad rychlé konfigurace modulu plánování rozpočtu a znázorňuje, jak lze provést plánování rozpočtu pomocí této konfigurace.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05de2748b0cf7a2b09618aee5c41c8c797f2b3d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210402"
---
# <a name="budget-planning"></a>Plánování rozpočtu

[!include [banner](../includes/banner.md)]

Cílem tohoto semináře je poskytnout přehled aktualizací funkcí aplikace Microsoft Dynamics 365 Finance v oblasti Plánování rozpočtu. Tento seminář ukazuje příklad rychlé konfigurace modulu plánování rozpočtu a znázorňuje, jak lze provést plánování rozpočtu pomocí této konfigurace.  Tento seminář se zaměřuje na následující obchodní procesy nebo úlohy:
- Vytvoření organizační hierarchie pro plánování rozpočtu a konfigurace zabezpečení uživatele
- Definování scénářů plánů rozpočtu, sloupců plánu rozpočtu, rozvržení a šablon aplikace Excel
- Vytvoření a aktivace procesu plánování rozpočtu
- Vytváření dokument plánu rozpočtu za použití skutečných hodnot z hlavní knihy
- Použití přidělení pro úpravu dat dokumentu plánu rozpočtu
- Úpravy dat dokumentu plánu rozpočtu v aplikaci Excel 

<a name="prerequisites"></a>Předpoklady 
------------------

Pro tento kurz budete potřebovat přístup k prostředí aplikace Microsoft Dynamics 365 Finance s ukázkovými daty Contoso a přiřazení k instanci jako správce. Pro tento seminář nepoužívejte soukromý režim prohlížeče – odhlaste se z jiného účtu v prohlížeči podle potřeby a přihlaste se pomocí údajů správce. Při přihlašování **MUSÍTE** zaškrtnout políčko „Zůstat přihlášen”. Tímto krokem zajistíte vytvoření trvalého souboru cookie, který aplikace Excel momentálně vyžaduje. Přihlašujete-li se k aplikaci pomocí jiného prohlížeče než IE, zobrazí se výzva k přihlášení v aplikaci Excel. Po kliknutí na tlačítko „Přihlásit” v aplikaci Excel se otevře místní okno IE a při přihlašování **MUSÍTE** zaškrtněte políčko „Zůstat přihlášeni”. Pokud se zdá, že volba „Přihlásit se” v aplikaci Excel nemá žádný účinek, vyprázdněte mezipaměť souborů cookie v IE.

## <a name="scenario-overview"></a>**Přehled scénáře**
Julie pracuje jako finanční manažerka společnosti Contoso Entertainment Systems v Německu (DEMF). S blížícím se fiskálním rokem 2016 potřebuje pracovat na nastavení rozpočtu společnosti pro nadcházející rok. Příprava rozpočtu vypadá takto:

1.  Julie použije skutečná množství z předchozího roku výchozí bod k vytvoření rozpočtu.
2.  Na základě skutečných hodnot z předchozího roku vytvoří odhady pro 12 měsíců v nadcházejícím roce.
3.  Julie projde rozpočet s finančním ředitelem. Po dokončení provádí nezbytné úpravy plánu rozpočtu a dokončuje přípravu rozpočtu.

Schéma konfigurace plánování rozpočtu pro scénář vypadá takto:

![Schéma konfigurace plánování rozpočtu](./media/screenshot1-300x152.png)

Julie používá následující šablonu aplikace Excel k přípravě rozpočtu:

[![Šablona aplikace Excel](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Cvičení 1: Konfigurace

### <a name="task-1-create-organizational-hierarchy"></a>**Úkol 1: Vytvoření organizační hierarchie**
Protože se proces rozpočtování odehrává ve finančním oddělení, Julie potřebuje vytvořit velmi jednoduchou organizační hierarchii tvořenou pouze finančním oddělením. 

1.1. Přejděte k Organizačním hierarchiím (Správa organizace &gt; Organizace &gt; Organizační hierarchie) a klikněte na tlačítko Nová.

![Organizační hierarchie](./media/screenshot3.png) 

1.2. Zadejte název organizační hierarchie do pole Název a klikněte na tlačítko Přiřadit účel.

1.3. Vyberte účel plánování rozpočtu, klikněte na tlačítko Přidat a přiřaďte nově vytvořenou organizační hierarchii. 

[![Přiřadit účel](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Zopakujte výše uvedený krok s účelem zabezpečení organizace. Po dokončení formulář zavřete.

1.5. Ve formuláři Organizační hierarchie klikněte na tlačítko Zobrazit. Klikněte na tlačítko Upravit v Návrháři hierarchie a vytvořte hierarchii kliknutím na tlačítko Vložit.

[![Vložit](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Vyberte Finanční oddělení pro hierarchii rozpočtování. 

[![Finance](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Po dokončení klikněte na tlačítko Publikovat a zavřít. Vyberte 1. 1. 2015 jako datum účinnosti pro publikování hierarchie.

[![Platný od](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Úkol 2: Konfigurace zabezpečení pro uživatele
Plánování rozpočtu používá zvláštní zásady zabezpečení pro konfiguraci přístupu k datům rozpočtových plánů. Julie musí udělit přístup k finančním plánům rozpočtu sama sobě. 

2.1. Přepněte do kontextu právnické osoby DEMF. 


2.2. Přejděte do části Rozpočtování &gt; Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu. Na kartě Parametry nastavte hodnotu Model zabezpečení na hodnotu Založeno na organizacích zabezpečení 

[![Parametry](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Přejděte do nabídky Správa systému &gt; Uživatelé &gt; Uživatelé. Přiřaďte uživateli Admin (Julii Funderburk) roli správce rozpočtu. 

[![Správce rozpočtu](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Vyberte roli uživatele a klikněte na tlačítko Přiřadit organizace. 

[![Přiřadit organizace](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Zvolte možnost „Udělit přístup ke specifickým organizacím”. Vyberte organizační hierarchii vytvořenou v prvním kroku. Vyberte finanční uzel a klikněte na tlačítko Udělit přístup s podřízenými organizacemi. 

***Důležité!** _ _Ujistěte se, že jste v kontextu právnické osoby DEMF při provádění tohoto úkolu, protože zabezpečení organizace se aplikuje za právnickou osobu* 

### <a name="task-3-create-scenarios"></a>Úkol 3: Vytvoření scénáře
3.1. Přejděte do části Rozpočtování&gt;Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu. Na stránce Scénáře si všimněte scénářů, které budeme později v tomto semináři používat: Skutečné hodnoty předchozího roku a Rozpočtováno 

*Poznámka: pokud chcete, můžete pro toto cvičení vytvořit a používat nové scénáře.* 

[![Nové scénáře](./media/screenshot15.png)](./media/screenshot15.png) 

*Poznámka: protože Julie nepoužívá formální schvalovací proces pro přípravu rozpočtu, přeskočíme v tomto semináři nastavení Workflowy, Fáze a Fáze workflowu a použijeme existující nastavení pro automatické schválení workflowu. Viz dodatek pro tuto konfiguraci workflow.*

### <a name="task-4-create-budget-plan-columns"></a>Úkol 4: Vytvoření sloupců plánu rozpočtu
Sloupce plánu rozpočtu jsou buď peněžní, nebo množstevní sloupce, které lze použít v rozvržení dokumentu plánu rozpočtu. V našem příkladu je nutné vytvořit sloupec pro skutečné hodnoty předchozího roku a 12 sloupců představujících každý měsíc rozpočtu předchozího roku. Sloupce lze vytvářet buď kliknutím na tlačítko Přidat a zadáním hodnot, nebo využitím datové entity. V tomto semináři použijeme datovou entitu k vyplnění hodnot. 

4.1. V části Rozpočtování&gt;Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu otevřete stránku Sloupce. Klikněte na tlačítko Office v pravém horním rohu formuláře a vyberte Sloupce (nefiltrováno). 

[![Nefiltrované sloupce](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Systém otevře sešit aplikace Excel pro vyplnění hodnot. Pokud se zobrazí výzva, klikněte na Povolit úpravy a Důvěřovat této aplikaci. 

4.3. Budeme potřebovat více sloupců k vyplnění hodnot. Klikněte na Návrh na pravém podokně pro přidání sloupců do mřížky. 

[![Návrh](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klikněte na symbol tužky vedle volby PlanColumns a zobrazte dostupné sloupce k přidání do mřížky. 

[![Upravit](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Dvojitým kliknutím na každé dostupné pole je přidáte k vybraným polím, a poté klikněte na tlačítko Aktualizovat. 

4.6. Do tabulky aplikace Excel přidejte všechny sloupců, které je třeba vytvořit. Použijte funkci automatického vyplňování v aplikaci Excel pro rychlé přidání řádků. Ujistěte se, že řádky jsou přidány jako součást tabulky (používáte-li svislý posuvník, měli byste vidět záhlaví sloupců v horní části mřížky). 

4.7. Vraťte se do aplikace a obnovte stránku. Zobrazí se publikované hodnoty. 

[![Znovu načíst](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Úkol 5: Vytváření rozvržení dokumentu plánu rozpočtu a šablon
Rozvržení definuje, jakým způsobem bude mřížka řádků dokumentu plánu rozpočtu vypadat, až uživatel otevře dokument plánu rozpočtu. Dále je možné přepnout rozvržení dokumentu plánu rozpočtu, aby se zobrazila stejná data v různých úhlech. Protože Julie definovala sloupce pro použití s dokumentem plánu rozpočtu, potřebuje nyní vytvořit rozvržení dokumentu plánu rozpočtu, které bude vypadat podobně jako tabulka aplikace Excel, kterou používá k vytvoření dat rozpočtu (viz část Přehled scénáře v tomto semináři) 

5.1. V části Rozpočtování&gt;Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu otevřete stránku Rozložení. Vytvořte nové rozvržení pro měsíční položku rozpočtu:

-   Vyberte sadu dimenzí MA+BU, abyste zahrnuli hlavní účty a obchodní jednotky do rozvržení.
-   Uveďte všechny sloupce plánu rozpočtu vytvořené v předchozím kroku v oddílu Prvky. Povolte úpravy u všech položek s výjimkou skutečných hodnot z předchozího roku.
-   Kliknutím na tlačítko Popisy vyberte finanční dimenze, které mají zobrazit popisy v mřížce.

[![Popisy](./media/screenshot24.png)](./media/screenshot24.png) 

Na základě definice rozložení plánu rozpočtu můžeme vytvořit šablonu aplikace Excel, která se použije jako alternativní způsob úpravy dat rozpočtu. Protože se šablona aplikace Excel musí shodovat s definicí rozložení plánu rozpočtu, nebude možné upravit rozložení plánu rozpočtu po generování šablony aplikace Excel. Proto tento úkol proveďte až po definování všech komponentů rozvržení. 

5.2. Pro rozvržení vytvořené 5.1. krok, klikněte na tlačítko Šablona &gt; Generovat. Potvrďte varovnou zprávu. Chcete-li zobrazit šablonu, klikněte na položku Šablona &gt; Zobrazit. 

*Poznámka: Je nutné vybrat možnost „Uložit jako” a vybrat umístění, kam se má šablona uložit, aby bylo možné ji upravit. Pokud uživatel vybere možnost „Otevřít” v dialogovém okně bez uložení změn, nebudou změny v souboru zachovány po zavření souboru..* 
[![Zobrazení šablony](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Nepovinný krok&gt; Upravte šablonu aplikace Excel, aby byla uživatelsky přívětivější – přidejte vzorce součtu, pole záhlaví, formátování atd. Uložte změny a odešlete soubor do rozvržení plánu rozpočtu kliknutím na možnost Rozvržení &gt; Odeslat. 


### <a name="task-6-create-a-budget-planning-process"></a>Úkol 6: Vytvoření procesu plánování rozpočtu
Julie potřebuje vytvořit a aktivovat nový procesu plánování rozpočtu spojením celého nastavení uvedeného výše, aby mohla začít zadávat plány rozpočtu. Proces plánování rozpočtu definuje, které rozpočtovací organizace workflow, rozvržení a šablony se použijí pro vytváření plánů rozpočtu. 

6.1. Přejděte do Rozpočtování &gt; Nastavení &gt; Plánování rozpočtu &gt; Proces plánování rozpočtu a vytvořte nový záznam.

-   Proces plánování rozpočtu – rozpočtování DEMF pro fiskální rok 2016
-   Rozpočtový cyklus – fiskální rok 2016
-   Hlavní kniha – DEMF
-   Výchozí účetní struktura – výroba zisků a ztrát
-   Organizační hierarchie – vyberte hierarchii vytvořenou na začátku semináře
-   Workflow plánování rozpočtu – přiřaďte Automatickém schválení workflow pro finanční oddělení
-   V pravidlech fází plánování rozpočtu a šablon u všech workflowů fáze plánování rozpočtu vyberte, jestli jsou přidávání řádků a úpravy řádků povolené a jaké rozvržení se má použít jako výchozí

*Poznámka: Můžete vytvořit další rozvržení dokumentu a zpřístupnit je ve fázi workflowu plánování rozpočtu kliknutím na tlačítko Alternativní rozložení.* 

[![Alternativní rozložení](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Vyberte Akce &gt; Aktivovat pro aktivaci tohoto workflow plánování rozpočtu. 

[![Aktivovat](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Cvičení 2: Simulace procesu

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Úkol 7: Generování počátečních dat pro plán rozpočtu z hlavní knihy
7.1. Přejděte do Rozpočtování &gt; Periodicky &gt; Generovat plán rozpočtu z hlavní knihy. Zadejte parametry periodického procesu a klikněte na tlačítko Generovat. 

7.2. Přejděte do Rozpočtování &gt; Plány rozpočtu a vyhledejte plán rozpočtu vytvoření v procesu generování. 

[![Plán rozpočtu](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Otevřete podrobnosti dokumentu kliknutím na odkaz Číslo dokladu. Plán rozpočtu se zobrazí podle definovaného rozvržení vytvořeného během tohoto semináře. 

[![Zobrazení plánu rozpočtu](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Úkol 8: Vytvoření rozpočtu pro aktuální rok podle skutečných hodnot předchozího roku
Metody přidělení lze použít v plánu rozpočtu ke snadnému kopírování informací pro plány rozpočtu z jednoho scénáře do jiného / jejich rozdělení do období / přidělení k dimenzím. Použijeme přidělení k vytvoření rozpočtu pro aktuální rok ze skutečných hodnot předchozího roku. 

8.1. Vyberte všechny řádky v mřížce dokumentu plánu rozpočtu a klikněte na tlačítko Přidělit rozpočet. 

[![Všechny řádky](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Vyberte metodu přidělení, klíč období, zdrojový a cílový scénář a klikněte na tlačítko Přidělit. 

[![Přidělit](./media/screenshot33.png)](./media/screenshot33.png)

Skutečné částky z předchozího roku se zkopírují do aktuálního rozpočtu a následně je lze přidělit napříč obdobími pomocí Klíče období křivky prodeje. 

[![Křivka prodeje](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Úkol 9: Úprava dokumentu plánu rozpočtu pomocí aplikace Excel a dokončení dokumentu
9.1. Klikněte na tlačítko List a otevřete obsah dokumentu v aplikaci Excel.

9.2. Po otevření sešitu aplikace Excel upravte čísla v dokumentu plánu rozpočtu a klikněte na tlačítko Publikovat.

9.3. Vraťte se k dokumentu plánu rozpočtu. Klikněte na tlačítko Workflow &gt; Odeslat dokument k automatickému schválení.

[![Automaticky schválit](./media/screenshot37.png)](./media/screenshot37.png) 

Po dokončení workflowu se fáze dokumentu plánu rozpočtu změní na Schváleno. [![Schváleno](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Dodatek

### <a name="auto-approve-workflow-configuration"></a>Konfigurace automatického schválení workflow

A. Rozpočtování &gt; Nastavení &gt; Plánování rozpočtu &gt; Workflow rozpočtování. Vytvořit nové workflow pomocí šablony workflow plánování rozpočtu:

[![Vytvořit nový workflow](./media/screenshot39.png)](./media/screenshot39.png)

Tento workflow bude obsahovat pouze jednu úlohu – Přechod fáze plánu rozpočtu. 

[![Přechod fáze plánu rozpočtu](./media/screenshot40.png)](./media/screenshot40.png) 

Uložte a aktivujte workflow. 

B. Přejděte do části Rozpočtování &gt; Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu. Na kartě Fáze vytvořte 2 fáze – Počáteční a Odesláno. 

[![Počáteční a odesláno](./media/screenshot41.png)](./media/screenshot41.png)

C. Přejděte do části Rozpočtování &gt; Nastavení &gt; Plánování rozpočtu &gt; Konfigurace plánování rozpočtu. Na kartě Fáze workflowu přidružte automatické schválení workflowu vytvořené v kroku A fázím Počáteční a Odesláno.

[![Tvorba rozpočtu a plánování rozpočtu](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]