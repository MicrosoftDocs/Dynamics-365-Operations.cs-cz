---
title: Přehled plánování rozpočtu
description: Toto téma popisuje plánování rozpočtu. Obsahuje informace, které vám pomohou při konfiguraci plánování rozpočtu a nastavení procesů plánování rozpočtu.
author: ryansandness
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3744fd823576b597b4550008338e3cc96cb585d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441282"
---
# <a name="budget-planning-overview"></a>Přehled plánování rozpočtu

[!include [banner](../includes/banner.md)]

Toto téma popisuje plánování rozpočtu. Obsahuje informace, které vám pomohou při konfiguraci plánování rozpočtu a nastavení procesů plánování rozpočtu.

## <a name="overview-of-budget-planning"></a>Přehled plánování rozpočtu

Organizace může nastavit plánování rozpočtu a poté nastavit procesy plánování rozpočtu pro potřeby splnění zásad a postupů a požadavků pro přípravu rozpočtu. Pokud rozumíte konceptům a terminologii, které se používají v aplikaci Microsoft Dynamics 365 Finance, bude pro vás snazší a efektivnější provádět plánování rozpočtu ve vaší organizaci.

### <a name="key-terms"></a>Klíčové podmínky

- **Procesy plánování rozpočtu** – procesy plánování rozpočtu určují způsob, jakým budou rozpočtové plány v organizační hierarchii rozpočtování aktualizovány, směrovány, revidovány a schváleny. Proces plánování rozpočtu je připojen k rozpočtovému cyklu organizace prostřednictvím právnické osoby.
- **Plány rozpočtu** – plány rozpočtu obsahují data rozpočtu pro rozpočtový cyklus. Můžete mít více plánů rozpočtu, které se používají k různým účelům. Plány rozpočtu lze použít například k vytvoření částek rozpočtu pro různé organizační jednotky. Lze je použít také k provádění porovnání a rozhodování.
- **Scénáře plánu rozpočtu** – scénáře plánu rozpočtu definují kategorie dat pro plány rozpočtu. Definujte scénáře plánu rozpočtu pro podporu peněžních tříd a jiných tříd jednotek měření, například množství. Scénáře peněžního plánu rozpočtu zahrnují například "Oddělení – předchozí rok" a "Požadavky oddělení". Příklady scénářů plánu rozpočtu používající množství zahrnují "Počet telefonátů podpory za předchozí rok" a "Počet ekvivalentů plných úvazků (FTE)".
- **Fáze plánování rozpočtu** – fáze plánování rozpočtu definují postup, který plán rozpočtu dodržuje od počátku až do konečného schválení. Fáze plánování rozpočtu jsou uspořádány do workflowu plánování rozpočtu.
- **Workflowy plánování rozpočtu** – workflowy plánování rozpočtu se skládají z fází plánování rozpočtu a definují je. Workflowy rozpočtového plánování jsou přidruženy k workflowům rozpočtování. Workflowy rozpočtování jsou automatizované a ruční procesy, které posunují plány rozpočtu do dalších fází plánování rozpočtu.

[![Terminologie plánování rozpočtu](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Typické úkoly

Pomocí plánování rozpočtu můžete provádět následující úkony:

- Vytvořte plány rozpočtu k definování očekávaných příjmů a výdajů pro rozpočtový cyklus.
- Analyzujte a aktualizujte plány rozpočtu pro více scénářů.
- Automaticky směrujte plány rozpočtu společně s listy, dokumenty odůvodnění a jinými přílohami ke kontrole a schválení.
- Konsolidujte více plánů rozpočtu z nižší úrovně organizace do jediného nadřazeného plánu rozpočtu na vyšší úrovni. Lze také vyvinout jeden plán rozpočtu na vyšší úrovni v organizaci a přidělit rozpočet nižším úrovním.

Plánování rozpočtu je integrováno s jinými moduly. Lze tedy zahrnout informace z předchozích rozpočtů, skutečných výdajů, dlouhodobého majetku a Lidských zdrojů. Protože je plánování rozpočtu také integrováno s aplikacemi Microsoft Excel a Microsoft Word, můžete tyto programy využít k práci s daty plánování rozpočtu. Například správce rozpočtu může exportovat požadavek oddělení rozpočtu ze scénáře plánu rozpočtu do listu aplikace Excel. Data lze pak analyzovat, aktualizovat a zobrazit na listě a pak opět publikovat do řádků plánu rozpočtu.

## <a name="configuring-budget-planning"></a>Konfigurace plánování rozpočtu

Funkce, která byla představena v Dynamics 365 Finance verze 10.0.9 (duben 2020), obsahuje funkci, která pomáhá zvýšit výkon při aktualizaci existujících záznamů v aplikaci Excel pomocí tlačítka **Publikovat** a následném jejich publikování zpět do klienta. Tato funkce urychluje proces aktualizace a také pomáhá snižovat pravděpodobnost, že dojde k zablokování aktualizace při současné aktualizaci mnoha záznamů. Chcete-li zpřístupnit tuto funkci, přejděte do pracovního prostoru **Správa funkcí** a zapněte funkci **Optimalizace dotazu plánování rozpočtu pro výkon** v modulu **Rozpočtování**. Doporučujeme, abyste tuto funkci zapnuli.

Stránka **Konfigurace plánování rozpočtu** obsahuje nastavení, která jsou vyžadována pro nastavení plánování rozpočtu. Následující části popisují některé klíčové faktory, které byste měli zvážit při konfiguraci plánování rozpočtu. Po dokončení konfigurace můžete nastavit procesy plánování rozpočtu.

### <a name="budget-planning-schema-optional"></a>Schéma plánování rozpočtu (volitelné)

Volitelný doporučený první krok je vytvořit schéma zobrazující postupy organizace k vypracování rozpočtu. K vytvoření tohoto schématu můžete použít jakoukoli metodu.

Následující obrázek znázorňuje obecný příkladu, kde jsou oddělené workflowy plánování rozpočtu vytvořené pro různé úrovně organizace. Fáze jsou definovány v rámci každého workflowu a konkrétní scénáře jsou přiřazené jednotlivým fázím k uchování dat rozpočtu. Úlohy jsou dokončeny k přesunu dat z jedné fáze do druhé. Například částky můžete přidělit nebo agregovat do různých účtů, schválení nebo jiných hodnocení. V této inlustraci kurzíva označuje scénář, který nelze upravit během fáze, nebo data, která jsou z minulosti nebo byla schválena v dřívější fázi, a proto by neměla být změněna.

[![Obecné schéma plánování rozpočtu](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Následující ilustrace ukazuje příklad, kdy vedení společnosti odhaduje základní částky prvotního základu rozpočtu a distribuuje je pro Prodejní oddělení. Prodejní oddělení pak odhadují a odesílají vlastní předpovědi zpět na ústředí, kde správce rozpočtu agreguje a upraví předpovědi. Správce rozpočtu nakonec odešle upravené částky rozpočtu vedoucímu finančního oddělení (CFO) pro kontrolu, konečné úpravy a k schválení.

[![Příklad schématu plánování rozpočtu](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organizační hierarchie pro plánování rozpočtu

Na stránce **Organizační hierarchie** lze určit organizační hierarchii jako hierarchii plánování rozpočtu pro každý procesu plánování rozpočtu. Plánování rozpočtu nemusí odpovídat standardní organizační hierarchii, která se používá pro jiné účely. Vzhledem k tomu, že tuto hierarchii lze použít k agregaci a distribuci dat, můžete jí dát jinou strukturu. V příkladu schématu jsou Prodejní oddělení pod úrovní centrály, která zahrnuje rozpočtové a finanční oddělení. Tato struktura se pravděpodobně liší od struktury, která se používá ke správě operací pro prodejní oddělení. Pouze jednu hierarchii plánování lze přiřadit ke každému procesu plánování rozpočtu.

Další informace viz [Organizace a organizační hierarchie](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Uživatelské zabezpečení

Plánování rozpočtu může dodržovat jeden ze dvou modelů zabezpečení k definici oprávnění uživatelů. Model zabezpečení určíte tak, že nastavíte parametr plánování rozpočtu na stránce **Konfigurace plánování rozpočtu**.

### <a name="budget-planning-workflows-stages"></a>Fáze workflowu plánování rozpočtu

Workflowy plánování rozpočtu se používají v kombinaci s workflowy rozpočtování pro správu tvorby a vývoje plánů rozpočtů.

Workflow plánování rozpočtu je tvořen uspořádanou sadou fází, kterými plán rozpočtu prochází. Každý workflow rozpočtového plánování je přidružen k workflowu rozpočtování. Workflowy rozpočtování jsou jedním z typů workflowů, které se používají v aplikaci Dynamics 365 Finance. Směrují plány rozpočtu spolu s listy, odůvodněním a přílohami prostřednictvím organizace k revizi a schválení.

Workflow plánování rozpočtu vytváříte v části **Fáze workflowu** na stránce **Konfigurace plánování rozpočtu**. Zde můžete vybrat fáze a workflowu rozpočtování, který bude použit, a vy nakonfigurujete další nastavení.

Je vhodné vytvořit workflow plánování rozpočtu pro každou úroveň hierarchie rozpočtování. Poté můžete přiřadit workflow rozpočtování, který obsahuje prvky, které odpovídají fázím workflowu plánování rozpočtu. V příkladu schématu zobrazeném v tomto tématu bude jeden workflow plánování rozpočtu vytvořen pro prodejní oddělení a jiný pro ústředí. Workflow rozpočtování přesune plány rozpočtu jednotlivými fázemi.

Workflow rozpočtování můžete vytvořit pro plánování rozpočtu na stránce **Workflowy rozpočtování**. Tento proces se podobá procesu vytváření jiných workflowů. Následující obrázek znázorňuje příklad workflowu pro ústředí.

[![Workflow rozpočtování pro plánování rozpočtu](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Workflow obsahuje následující prvky:

- Přidělení k oddělení prodeje a agregace jejich odeslání
- Kontrola manažera rozpočtu
- Achválení CFO
- Fázování přechodů mezi jednotlivými fázemi workflowu plánování rozpočtu

Workflow rozpočtování přiřazujete v každému workflow plánování rozpočtu v části **Fáze workflowu** na stránce **Konfigurace plánování rozpočtu**.

### <a name="parameters-scenarios-and-stages"></a>Parametry, scénáře a fáze

Počáteční nastavení na stránce **Konfigurace plánování rozpočtu** vám umožní vytvořit některé stavební bloky pro další kroky konfigurace:

- **Parametry** – parametry definují pravidla zabezpečení, která chcete použít pro plány rozpočtu, a výchozí finanční dimenze, které se mají použít, když uživatelé přecházejí k podrobnostem částek ve scénářích plánu rozpočtu.
- **Scénáře** – scénáře zahrnují kategorie dat, které chcete použít pro plány rozpočtu. Definujte scénáře plánu rozpočtu pro podporu peněžních tříd a jiných tříd jednotek měření, například množství. V plánu rozpočtu představují scénáře jednu verzi dat plánování rozpočtu. Scénáře peněžního plánu rozpočtu zahrnují například "prodeje v předchozích letech" a "podepsané smlouvy". Příklady scénářů, které používají množství, zahrnují "počet prodejních telefonátů" a "počty ekvivalentů plných úvazků (FTE)".
- **Fáze** – fáze definují kroky, které plán rozpočtu prochází od počátku po konečný souhlas. Příklady fází plánování rozpočtu zahrnují "kumulaci ústředí", "revize finančního ředitele" a "konečný".

### <a name="allocation-schedules"></a>Plány přidělení

Ve plánování rozpočtu můžete přidělit částky nebo množství na řádcích plánu rozpočtu z jednoho scénáře do jiného nebo dokonce stejné scénáře. Například můžete přidělovat ve stejném scénáři částky nebo množství, pokud provedete změny finanční dimenze nebo dat částek v daném scénáři. Přidělení lze provést v rámci plánu rozpočtu nebo z jednoho plánu rozpočtu do druhého.

Plány přidělení automaticky přiřazují řádky plánu rozpočtu během workflowu zpracování. Přidělení lze provádět pomocí některé z následujících metod v seznamu **Metody přidělení**:

- **Přidělit napříč obdobími** – alokační klíč období se používá k přidělení řádků plánu rozpočtu ze zdrojového scénáře plánu rozpočtu napříč obdobími v cílovém scénáři.

    > [!NOTE]
    > Před přidělením napříč obdobími je nutné nastavit alokační klíče období na stránce **Kategorie přidělení období**.

- **Přidělit k dimenzím** – řádky plánu rozpočtu jsou přiděleny ze zdrojového scénáře plánu rozpočtu napříč finančními dimenzemi v cílovém scénáři.

    > [!NOTE]
    > Dříve než začnete přidělovat dimenze, je nutné nastavit podmínky přidělení rozpočtu na stránce **Podmínky přidělení rozpočtu**.

- **Agregovat** – řádky plánu rozpočtu jsou agregovány ze zdrojového scénáře plánu rozpočtu v přidruženém plánu rozpočtu do cílového scénáře v nadřazeném rozpočtovém plánu.
- **Rozdělit** – řádky plánu rozpočtu jsou distribuovány ze zdrojového scénáře plánu rozpočtu v nadřazeném plánu rozpočtu do cílového scénáře v souvisejících rozpočtových plánech.
- **Použít pravidla přidělení hlavní knihy** – řádky plánu rozpočtu jsou rozděleny ze zdrojového scénáře plánu rozpočtu do cílového scénáře na základě vybraného pravidla přidělení hlavní knihy.
- **Kopírovat z plánu rozpočtu** – můžete vybrat jiný plán rozpočtu, který se má použít jako zdroj přidělení.

### <a name="stage-allocations"></a>Přidělení fází

Fáze přidělení lze použít k automatickému přidělení řádků plánu rozpočtu během zpracování workflowu. Když se používají fáze přidělení, řádky plánu rozpočtu v cílovém scénáři lze vytvořit a upravit bez zásahu osoby, která připravila plán rozpočtu nebo kontrolora.

Při nastavení přidělení fáze můžete přiřadit workflow a fázi plánu rozpočtu k plánu přidělení. Workflow plánování rozpočtu je nutné přiřadit k workflowu rozpočtování, který používá automatickou úlohu workflowu **Přidělení fáze plánování rozpočtu**. Když workflow dosáhne určité fáze, dojde k automatickému přidělení. Tato automatizovaná úloha slouží k vytvoření řádků plánu rozpočtu v novém scénáři.

V příkladu schématu zobrazeném dříve v tomto tématu je přidělení provedeno k převodu částek z plánu rozpočtu a scénářů v "základní" fázi ústředí do jiného plánu rozpočtu a scénářů obchodních oddělení ve fázi "odhadu". Následující obrázek ukazuje příslušnou část ilustračního schématu.

[![Přidělení fází](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Navíc se v příkladu schématu provádí agregace z plánů rozpočtu a scénářů prodejních oddělení ve fázi "odesláno" v nadřazeném plánu v "kumulativní" fázi ústředí. Následující obrázek ukazuje příslušnou část ilustračního schématu.

[![Agregace](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Priority

Lze volitelně použít plánu rozpočtu k definování kategorií a cílů pro plány rozpočtu, které jste vytvořili. Lze také použít priority k uspořádání, klasifikaci a vyhodnocení více plánů rozpočtu. Například můžete vytvořit prioritu plánování rozpočtu pro zdraví a bezpečnost, a poté vyhodnotit plány rozpočtu přiřazené k dané prioritě. Můžete také přiřadit k plánům rozpočtu číslo a vyznačit tak hodnocení.

### <a name="columns-and-layouts"></a>Sloupce a rozvržení

Hodnoty rozpočtu se zobrazí v řádcích a sloupcích plánu rozpočtu. Je nutné nejprve definovat sloupce a poté můžete vytvořit rozvržení k definování prezentace sloupců.

Chcete-li definovat sloupec, vyberte scénář plánu rozpočtu. Částky řádku z tohoto scénáře jsou zobrazeny v plánu rozpočtu. Můžete vybrat období pro filtrování částky a lze také použít filtry, které jsou založeny na účtu hlavní knihy.

Když definujete rozvržení, vyberte sadu dimenzí hlavní knihy, abyste vytvořili řádky plánu rozpočtu, které chcete zobrazit, a vyberte sloupce jako prvky rozložení. Můžete vytvořit více rozložení, takže plán rozpočtu zobrazí požadovaná data v různých fázích daného procesu plánování rozpočtu.

Kromě sloupce částek rozpočtu můžete definovat sloupce pro pole projekt, navrhovaný projekt, majetek a pole navrhovaný majetek z plánu rozpočtu. Můžete také definovat sloupce pro rozpočtové pozice. Tato možnost je užitečná při analýze rozpočtů personálu.

U ukázkového schématu můžete chtít vytvořit sloupce pro scénáře "prodeje PY", "smlouvy" a "prognóza". (Následující ilustrace ukazuje příslušnou sekci schématu). Můžete pak rozdělit jeden nebo všechny z uvedených scénářů do samostatných sloupců za každé čtvrtletí fiskálního roku, takže správce oddělení prodeje může přesně zadávat prognózy částek pro každé období.

[![Sloupce](./media/columns.png)](./media/columns.png)

Rovněž určujete, zda každý prvek rozvržení (sloupec), lze upravit a zda je k dispozici v kterékoli šabloně listu, která je vytvořená pro toto rozvržení. V příkladovém schématu v rozložení použitém pro fáze "odhadu" lze upravovat sloupce "prognózy", zatímco sloupce "Prodeje PY" a "Smlouvy" jsou jen pro čtení.

> [!NOTE]
> Ve výchozím nastavení budete mít omezení na 36 sloupců, což vám umožní rozšířit plánování rozpočtů protřednictvím kroků v části [Rozšíření rozvržení plánování rozpočtu](./extending-budget-planning-layout.md).

### <a name="templates"></a>Šablony

V části **Rozvržení** na stránce **Konfigurace plánování rozpočtu** lze také vygenerovat, zobrazit nebo odeslat šablony aplikace Excel pro každé rozvržení. Tyto šablony jsou sešity spojené s každým plánem rozpočtu k poskytnutí další analýzy, grafů a možností pro zadání dat.

Když se šablona generuje, rozvržení je uzamčeno a nelze jej upravit. Toto uzamknutí pomáhá zajistit, aby formát šablony odpovídal rozvržení plánu rozpočtu a obsahovat stejné údaje. Po vygenerování šablony ji lze zobrazit a upravit. Můžete například do šablony přidat grafy nebo dále upravit její vzhled.

> [!NOTE]
> Šablona by měla být uložena do umístění, ke kterému má uživatel přístup, aby ji bylo možné odeslat do rozvržení po dokončení úprav. Tímto způsobem se šablona použije s plány rozpočtu, které používají rozvržení.

### <a name="descriptions"></a>Popisy

V části **Rozvržení** lze přiřazit popisy, které slouží ke zobrazení názvu finanční dimenze, která je zahrnuta do rozvržení. Organizace může například chtít zobrazit název hlavního účtu vedle čísla hlavního účtu v plánu rozpočtu. Může však chtít vynechat názvy jiných finančních dimenzí, aby se zabránilo neplnění zobrazení.

## <a name="setting-up-budget-planning-processes"></a>Nastavení procesů plánování rozpočtu

Po dokončení konfigurace plánování rozpočtu můžete nastavit procesy plánování rozpočtu na stránce **Proces plánování rozpočtu**. Procesy plánování rozpočtu jsou sady pravidel, která určují způsob, jakým budou rozpočtové plány v organizační hierarchii rozpočtování aktualizovány, směrovány, revidovány a schváleny.

Vyberte nejprve cyklus rozpočtu a hlavní knihu pro každý proces plánování rozpočtu. Každý proces plánování rozpočtu souvisí pouze s jedním rozpočtovým cyklem a jednou hlavní knihou. Poté vyberte organizační hierarchii rozpočtu na pevné záložce **Správa procesu plánování rozpočtu** a přiřaďte ke všem centrům odpovědnosti v organizaci, která se zobrazí v mřížce, workflow plánování rozpočtu.

Pokud chcete přiřadit nebo změnit workflow plánování rozpočtu pro podobná centra odpovědnosti, vyberte **Přiřadit workflow** a vyberte typ organizace pro cíl a workflow plánování rozpočtu, který chcete použít. ID workflowu rozpočtování, které je přiřazeno k jednotlivým workflowům plánování rozpočtu, je automaticky přidáno do mřížky.

Když definujete pravidla fáze a šablony na pevné záložce **Pravidla a rozložení fáze plánování rozpočtu**, můžete definovat jinou sadu pravidel a výchozí rozložení pro jednotlivé fáze plánování rozpočtu. Například fázi "odhadu" oddělení prodeje může umožnit uživatelům upravit řádky v plánu rozpočtu, ale zabránit uživatelům v přidávání řádků. Stav "Odesláno" může povolit uživatelům zobrazení řádků, ale nikoli přidání nebo úpravu, protože práce v této fázi je dokončena a změnám v plánech rozpočtů se musí zabránit. Pro výběr rozložení, která jsou k dispozici pro plány rozpočtu, vyberte **Alternativní rozložení**.

Volitelně můžete vybrat priority plánování rozpočtu na pevné záložce **Omezení priorit plánu rozpočtu**. Priority lze vybrat v plánech rozpočtu.

Posledním krokem je aktivace procesu plánování rozpočtu pomocí nabídky **Akce**. Proces plánování rozpočtu lze použít až po aktivaci.

V nabídce **Akce** je také možné vytvořit proces zkopírováním existujícího procesu. Tato funkce je užitečná pro organizace, které dodržují stejný postup pro každý rozpočtový cyklus a provádějí minimum změn nebo žádné změny.

Další užitečný příkaz v nabídce **Akce** je **Zobrazit stav zpracování rozpočtu**. Tento příkaz graficky zobrazí plány rozpočtu v rámci procesu spolu s odpovídajícími daty, jako jsou například stav workflowu plánů, souhrny podle množství a jednotky a navigace jedním kliknutím k samotným plánům rozpočtu.

[![Stav procesu plánování rozpočtu](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]