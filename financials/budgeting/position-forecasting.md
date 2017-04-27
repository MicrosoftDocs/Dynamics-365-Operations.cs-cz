---
title: "Prognóza pozic"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 1bc458d58834be1e2e9b602619f76424b3bb449b
ms.lasthandoff: 03/31/2017


---

# <a name="position-forecasting"></a>Prognóza pozic

[!include[banner](../includes/banner.md)]




Výdaje, které souvisejí s pracovníky, často tvoří velkou část nákladů organizace. Prognózy pozic vám umožní plánovat výdaje a zahrnut je do plánování rozpočtů.

## <a name="position-forecasting-in-budget-planning"></a>Prognóza pozic v plánování rozpočtu

[![Grafika nahoře](./media/graphic-top.png)](./media/graphic-top.png) 

Prognóza pozic používá tři hlavní složky pro zajištění přesných rozpočtových částek pro výdaje na pozice. Tyto částky mohou být potom přeneseny do plánu rozpočtu pro výpočty rozpočtu. 

Primární komponenta je **prognóza pozice**, která představuje všechna data nákladů, která se vztahují k jedné pozici. Přiřazením jiných scénářů plánu rozpočtu pro každou verzi můžete vytvořit několik verzí prognózy pozic. Více verzí umožňuje opakovaný přístup k rozpočtování a porovnávání pravděpodobnostních scénářů. Jednotlivé prognózy pozic mají odpovídající pozici v modulu Lidské zdroje.

**Prvek rozpočtových nákladů** je součást nastavení, která představuje konkrétní náklady, které jsou přiřazeny k pozici, jako například základní mzda, zdravotní pojištění placené zaměstnavatelem, náhrady pro mobilní telefon a tak dále. Prvek rozpočtových nákladů zahrnuje hlavní účet, který se používá pro náklady a možnosti výpočtu. Každý prvek rozpočtových nákladů lze přiřadit více pozicím prognózy. 

**Skupina kompenzací** je volitelná součást nastavení, kterou lze využít pro použití sady prvků rozpočtových nákladů a výpočet pozic, které mají podobné vlastnosti mzdy. Skupina kompenzací může zahrnovat mřížku kompenzací mzdové sazby. Pokud je skupina přiřazena k pozici prognózy, úroveň a krok v mřížce mohou přiřadit příjmy z pozice prognózy. Sada nákladových prvků je přidána automaticky.

### <a name="position-forecasting-processes"></a>Zpracování prognózy pozic

[![graphic1b](./media/graphic1b.png)](./media/graphic1b.png) 

V typickém procesu prognózy pozic nejprve vytvoříte součásti nastavení (prvky rozpočtových nákladů a skupiny kompenzací). Pozice prognóz, které se pak vytvoří, jsou založené na existujících pozicích. Poté můžete provést úpravy. Můžete například přidat nebo ukončit pozice, změnit mzdové sazby a náklady na zaměstnanecké výhody a přidat zvyšování mzdy. Můžete vytvořit více verzí prognózy pozic a usnadnit tak porovnání různých scénářů rozpočtování. Dále lze zahrnout pozice prognózy do plánů rozpočtu a přinést náklady z pozic prognózy jako řádky plánu rozpočtu.

Můžete vytvořit další verze pozic prognózy v rámci revize plánů rozpočtu. Tyto nové verze poskytují základ pro revize.

## <a name="position-forecasting-setup"></a>Nastavení prognózy pozic
[![graphic2](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Prvky rozpočtových nákladů

Prvky rozpočtových nákladů slouží k definování nákladových podrobnosti pro pozici prognózy. Tyto informace zahrnují typ nákladů, postup výpočtu nákladů a to, zda jsou náklady rozděleny do několika dat, když je pozice prognózy součástí plánu rozpočtu. 

Zvláštní pole definují chování prvku rozpočtových nákladů. Každému prvku rozpočtových nákladů je přiřazen typ rozpočtových nákladů **Příjem**, **Zaměstnanecké výhody**, **Daně** nebo **Jiné**. Typy rozpočtových nákladů se primárně používají k výpočtu součtů. Hodnota **Přepsání pozice prognózy** určuje, zda částky v prvku lze pro pozici prognózy upravit. Pole **Metoda přidělení** se používá, když je pozice prognózy přidána do plánu rozpočtu. Můžete rozdělit částky nákladů na samostatné řádky plánu rozpočtu s různými daty na základě měsíčního, čtvrtletního, týdenního nebo čtrnáctidenního intervalu. Výběrem počátečního data přiřadíte náklady jako jednu částku v den začátku nastavený pro tuto pozici prognózy. 

Výpočet částky nákladů pro prvek rozpočtových nákladů používá data platnosti a umožňuje tak použití stejného prvku nákladů v různých obdobích. V každém období je přiřazen jeden hlavní účet společně s procentuální hodnotou nebo roční částkou, která určuje částku nákladů. Prvek rozpočtových nákladů může používat procenta dalších prvků nákladů nebo částku za rok, nikoli však obojí. Můžete také určit roční limit. 

Pokud je nákladový prvek určen na základě procenta, je nutné zadat prvky rozpočtových nákladů, které se používají jako základ pro výpočet.

**Příklad** 

Organizace Jodi poskytuje náhrady na školení v rozsahu 5 procent základní mzdy zaměstnance. Jodi chce vytvořit prvek rozpočtových nákladů pro tyto náklady. Vytvoří nový prvek rozpočtových nákladů a přiřadí typ rozpočtových nákladů **Zaměstnanecké výhody**.

Jodi nechce, aby vedoucí pracovníci měnili množství zaměstnanecké výhody. Proto vybere **Nepovolovat změny nákladů** v poli **Přepsání pozice prognózy**. Organizace chce tyto náklady rozdělit rovnoměrně do každého měsíce. Jodi proto vybere **Čtvrtletně** v poli **Metoda přidělení**. 

Dále Jodi přidá řádek výpočtu nákladů, nastaví data a hlavní účet a zadá **5,00** jako procento. Její oddělení má rozpočet ve výši 5 000 USD za rok pro tuto zaměstnaneckou výhodu. Proto Jodi zadá tuto částku jako roční limit. 

Nakonec Jodi přidá všechny nákladové prvky příjmů, které slouží jako základ pro výpočet základu. Její prvek rozpočtových nákladů je nyní připraven pro použití.

### <a name="compensation-groups"></a>Skupiny kompenzací

Skupiny kompenzací lze použít k seskupení pozic prognózy, které mají podobné atributy kompenzace. Ty můžete také použít k definování příjmy nebo roční navýšení pozice prognózy a přiřazení sady společných prvků rozpočtových nákladů. 

Základní funkce skupin kompenzací je přiřazení sady prvků rozpočtových nákladů k pozici prognózy. Proto skupiny kompenzací slouží k přidání běžných nákladů, jako jsou například plány zaměstnaneckých výhod a daně. Například manažer, který vytvořil pozici prognózy, nemusí znát všechny nákladové prvky, které musí být přidány. Místo toho nákladové prvky lze přidat při výběru skupiny kompenzací. Prvky jsou přidány do nastavení skupiny kompenzace na kartě **Prvky rozpočtových nákladů**. 

Skupiny kompenzací mohou také určit sazby příjmů pro pozici prognózy. Provedete nastavení skupiny tak, aby používala hodinovou nebo roční mzdu pro výpočet příjmů pozice prognózy. Na kartě **Tabulky sazeb kompenzací** mřížka kompenzací mzdové sazby určuje příjmy, které jsou přidány do pozice prognózy, na základě přiřazené úroveň a kroku. Tyto mřížky mohou být založeny na existujících kompenzačních mřížkách v modulu Lidské zdroje. Můžete také vytvořit nové mřížky kompenzací pro plánování rozpočtu. 

Data platnosti a data vypršení platnosti v tabulkách sazeb kompenzace umožňují změnit mzdové sazby na libovolné datum. Tato funkce je užitečná zejména když oddělení pro vyjednávání sjednalo obecné navýšení uprostřed rozpočtového cyklu. V tomto případě změníte datum vypršení platnosti existující tabulky na den před datem změny sazby a přidat novou tabulku sazeb, která začíná novým datem. Když vytvoříte novou tabulku sazeb a vyberete **Vytvořit novou mřížku kompenzací z existující mřížky**, můžete vybrat existující tabulku sazeb z lidských zdrojů. V tabulce sazeb, které byla vytvořena, umožňuje možnost **Hromadná změna** použít procento nebo přímý objem zvýšení nebo snížení všech sazeb v mřížce. 

Pole **Plán zvýšení** a **Datum zvýšení** ve skupině kompenzací se používá, když musíte vytvořit zvyšování mzdy, protože pozice přechází z jednoho kroku na další. Roční zvýšení mzdy je typický scénář. Plán zvýšení určuje, zda se pro zvýšení kroku použije datum výročí pozice nebo jedno společné datum. Plán zvýšení platí pro všechny pozice prognózy ve skupině kompenzací. 

Nákladový prvek příjmů vybraný ve skupině kompenzací se používá při vytváření příjmů pro pozice prognózy ve skupině, včetně základní mzdy a jakéhokoli zvýšení kroku. Pole **Plán fixní kompenzace** odkazuje skupinu kompenzací na plán fixních kompenzací v modulu Lidské zdroje. Tento odkaz umožňuje přiřadit informace o fixní kompenzaci pracovníka k pozici prognózy a proto umožňuje provádět plánování rozpočtu přesněji. Mějte na paměti, že struktura kompenzační mřížky (úrovně a kroky) pro skupinu kompenzací musí odpovídat struktuře plánu fixní kompenzace. V opačném případě systém nemůže správně propojit skupinu kompenzací s plánem fixní kompenzace.

## <a name="creating-forecast-positions"></a>Vytváření pozic prognózy
[![graphic3](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Vytváření pozic prognózy pro existující pozice

Pro nejpřesnější plánování rozpočtu můžete vytvořit pozice prognózy využívající podrobných údajů z aplikace Microsoft Dynamics 365 for Operations, bez ohledu na to, zda je pozice aktuálně zaplněna nebo nezaplněna. 

Funkce **Přidat existující pozice** zobrazí všechny pozice pro organizaci. Pomocí nastavení pole** K datu** lze seznam pozic změnit tak, aby obsahoval pozice, které existovaly k datu v minulosti nebo, běžněji, v budoucnosti (například k začátku dalšího rozpočtového cyklu). Vyberte proces plánování rozpočtu a scénář plánu rozpočtu, vyberte pozice v seznamu a klepněte na tlačítko **OK** pro vytvoření pozic prognózy pro vybrané pozice. Všimněte si, že lze vytvořit pouze jednu pozici prognózy pro každou existující pozici v procesu plánování rozpočtu a scénáři. Přiřazením odlišných scénářů plánu rozpočtu však můžete vytvořit další verze. 

Pokud byly prvky rozpočtových nákladů přiřazeny k pozici v lidských zdrojích, tyto prvky rozpočtových nákladů jsou také přiřazené k pozici prognózy a používají výchozí částky. Pole **Přiřazený pracovník** pro pozici prognózy je nastaveno na jméno pracovníka, který je přiřazený k pozici (pokud je zaměstnanec přiřazen). Toto pole je prosté textové pole. Neproběhlo vytvoření žádného propojení. 

Je-li vybrán prvek rozpočtových nákladů, roční částka fixní kompenzace je přiřazena k pozici prognózy s použitím vybraného nákladového prvku, a to za předpokladu, že přiřazený pracovník má plán fixní kompenzace. Pokud pracovník nemá plán fixní kompenzace, nebo žádný pracovník není přiřazen, používá se pro prvek rozpočtových nákladů výchozí hodnota. 

Pokud je možnost **Přiřadit skupinu kompenzací** nastavena na **Ano** a pokud pracovník, který je přiřazený k pozici, má plán fixní kompenzace na základě kroku, který je připojen ke skupině kompenzací (popsané dříve), úroveň a krok pracovníka jsou přiřazeny k pozici prognózy spolu se skupinou kompenzací. Prvek rozpočtových nákladů příjmů ze skupiny kompenzací je přidán k pozici prognózy a používá se mzdová sazba na úrovni a kroku ze skupiny kompenzací. 

Nastavení možnosti **Přiřadit skupinu kompenzací** má přednost před nastavením **Přiřazení prvku rozpočtových nákladů**. Tato dvě nastavení lze použít současně. 

[![graphic4](./media/graphic4.png)](./media/graphic4.png) 

Další možností je přiřadit datum výročí. Vybrané datum (upravené datum zahájení, počáteční datum pracovníka, počátečním datum zaměstnání nebo datum zahájení služebního věku) přiřazeného pracovníka je nastaveno jako datum výročí pozice prognózy a slouží pouze pro informativní účely při vygenerování navýšení platby.

### <a name="creating-new-forecast-positions"></a>Vytváření nových pozic prognózy

Nové pozice prognózy můžete vytvořit dvěma způsoby: zkopírováním existující pozice prognózy a vytvořením zcela nové pozice prognózy. 

Pokud je vybrána pozice prognózy, výběrem možnosti **Kopírovat vybranou pozici prognózy** vytvořte novou pozici prognózy, který má stav prognózy **Navrhované**. Tato pozice prognózy má všechna data stejná, jako pozice prognózy, která byla zkopírována, s výjimkou přiřazeného pracovníka a poznámek k prvkům rozpočtových nákladů. Všimněte si, že odpovídající nová pozice je rovněž vytvořena v modulu Lidské zdroje. Tato pozice má popis **Vytvořeno prognózou**. 

Také můžete vytvořit zcela novou pozici prognózy. Vyberte existující úlohu a dále vyberte proces plánování rozpočtu a scénář plánu rozpočtu. Poté můžete přidat další podrobnosti, které chcete přidat. Zároveň se znovu vytvoří nová pozice v modulu Lidské zdroje.

## <a name="working-with-forecast-positions"></a>Práce s pozicemi prognózy
[![graphic5](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Více verzí pozice prognózy

Pozice prognózy můžete změnit a buď tak použít změny pro rozpočtový cyklus nebo modelování navržených změn. Běžným postupem je vytvořit základní sadu pozic prognózy, vytvořit kopie těchto pozic prognózy a pak použít kopie pro modelování různých sad změn. Kopie jsou přiřazeny do jiného scénáře plánu rozpočtu, ale přinejmenším do provedení změn jsou jinak shodné s pozicemi prognózy, ze kterých jsou zkopírovány. Originály a kopie sdílejí stejnou pozici v modulu Lidské zdroje. 

Tyto možnosti nabízí funkce **Kopírovat do scénáře**. Nezapomeňte, že jednotlivé pozice lidských zdrojů mohou mít pouze jednu pozici prognózy v každém scénáři plánu rozpočtu.

### <a name="modifying-forecast-positions"></a>Úprava pozic prognózy

Změny provedené v pozicích prognózy jsou omezeny na tyto pozice prognózy. Změny neovlivní záznamy pozice v modulu Lidské zdroje. Většina změn je také omezena na pozici prognózy, která je zpracovávána. Jinak řečeno změny jsou specifické pro proces plánování rozpočtu a scénář plánu rozpočtu, které jsou přiřazeny. Výjimku tvoří změny polí, která jsou sdílena u pozic v rámci procesů a scénářů. Tato pole zahrnují pole na kartě **Obecné** a **Finanční dimenze**. Při změně těchto polí budou nové hodnoty použity u pozice ve všech scénářích plánování rozpočtu. Z toho vyplývá, že tato pole umožňují rychle aktualizovat všechny verze.

#### <a name="budget-cost-elements"></a>Prvky rozpočtových nákladů

Prvky rozpočtových nákladů nabízí hlavní informace o plánech rozpočtu: částky rozpočtu a hlavní účet. Částka rozpočtu je částka, která je odeslána do plánu rozpočtu, když je pozice prognózy zahrnuta v plánu. Částka rozpočtu se vypočítává a nemůže být změněna přímo. Tato hodnota představuje roční částku nebo výpočet procenta prvků základu pro roční částku (jak je definováno v nastavení prvku rozpočtových nákladů). Částka je pak vynásobena počtem dnů v datovém rozsahu prvku (od počátečního data po datum ukončení) a také hodnotou **Ekvivalent plného úvazku** (FTE) pro tuto pozici prognózy. 

Například řádek prvku rozpočtových nákladů od 1. ledna 2017 do 30. června 2017 s roční částkou 100 000 a hodnotou FTE **0,50** se počítá jako 100 000 × (181 dnů ÷ 365 dnů) × 0,50 = 24 794,52. 

Při změně hodnoty FTE v pozici prognózy je nutno přepočítat řádky prvku rozpočtových nákladů. Řádky musí být přepočítány také při změně dat aktivace nebo dat odchodu do důchodu. Změny těchto dat mohou způsobit aktualizaci počátečního a koncového data prvku rozpočtových nákladů, které musí spadat do rozsahu dat v pozici prognózy. Pokud je vyžadováno přepočítání, tlačítko **Přepočítat** bude k dispozici a bude zobrazena zpráva "Vyžaduje se výpočet". Přepočítání je také vyžadováno, pokud chcete přidat nebo odebrat prvek rozpočtových nákladů.

**Příklad** 

Organizace zvažuje dvě možnosti snížení nákladů na účetní pozici. Jedna z možností je ukončení pozice v průběhu roku. Další možností je změna pozice na poloviční dobu pro celý rok. Brad vytvořil pozici prognózy pro existující pozici účetní v základním scénáři. Zkopíroval tuto základní pozici prognózy do scénáře A, nastavil datum vyřazení na 31. května a provedl přepočet. Poté Brad zkopíroval základní pozici prognózy do scénáře B, změnil hodnotu FTE na **0,50**a provedl přepočet. Brad má nyní tři verze, z nichž každá má celkové náklady, které jsou zarovnány s jeho možnostmi.

#### <a name="assigning-a-compensation-group"></a>Přiřazení skupiny kompenzací

Při prvním přiřazení skupiny kompenzace k pozici prognózy budou přidány výchozí prvky rozpočtových nákladů ze skupiny kompenzací. Pokud jsou nákladové prvky jsou přiřazeny k pozici prognózy, tyto prvky nákladů zde zůstanou. Pokud skupina kompenzací již byla přiřazena a došlo k její změně, stávající prvky rozpočtových nákladů budou odebrány a nahrazeny sadou ze skupiny kompenzací. 

Při výběru kompenzační úrovně a kroku bude přidán prvek rozpočtových nákladů příjmů (podle definice ve skupině kompenzací). Roční částka je vypočtena s použitím sazby ve vybrané úrovni a kroku a ročně odpracovanými hodinami ve skupině kompenzací (nebo pro roční mzdy celou částkou na úrovni a kroku). Tato částka se znovu vynásobí podle rozsahu dat na řádku nákladového prvku a hodnotou FTE z pozice prognózy.

#### <a name="generating-increases"></a>Generování zvýšení

Roční navýšení (jedno pro kalendářní rok) lze vytvořit automaticky pro pozice prognózy, které mají přiřazeny skupinu kompenzace podle kroku. Klepnutím na tlačítko **Generovat zvýšení** lze přidat prvek rozpočtových nákladů příjmů na dalším nejvyšším kroku. Počáteční datum nového prvek rozpočtových nákladů příjmů je plánované datum zvýšení uvedené na pozici prognózy. Toto datum je nastaveno ze skupiny kompenzací jedním ze dvou způsobů. Pokud je plán zvýšení u skupiny kompenzací nastaven na **Společné datum**, datum zvýšení je určeno ve skupině kompenzací. Pokud je plán zvýšení nastaven na **Datum výročí**, použije se pole s datem výročí pro pozici prognózy a rozpočtový cyklus dodává rok. Pokud existuje více kalendářních roků v rozpočtovém cyklu, bude přidáno více zvýšení. 

Koncové datum aktuálního prvku rozpočtových nákladů příjmů je aktualizováno dnem před datem zvýšení. Proces přepočtu se automaticky použije při generování zvýšení. Z tohoto důvodu není nutné přepočítávat ručně. 

Pokud klepnete na tlačítko **Generovat zvýšení** podruhé, proces se spustí znovu, ale nepřidá další záznamy. Je vytvořeno pouze jedno zvýšení za každý kalendářní rok.

#### <a name="changes-from-other-pages"></a>Změny z ostatních stránek

Aktualizace pozic prognózy mohou také pocházet z ostatních oblastí, jako jsou stránky s nastavením prvků rozpočtových nákladů a skupiny vyrovnání. Můžete také upravit pozice prognózy pomocí procesu hromadné aktualizace. 

Na stránce s nastavením **Prvek rozpočtových nákladů** jsou dostupné dvě možnosti: **Přidat do pozic** a **Aktualizovat pozice**. Možnost **Přidat do pozic** přidá prvek rozpočtových nákladů do vybraných pozic prognózy. Pokud prvek již byl přiřazen k pozici prognózy, tato pozice prognózy bude vynechána. Možnost **Aktualizovat pozice** použije aktuální hodnoty (hlavní účet, procento, roční částku a tak dále) na vybrané pozice prognózy. 

Každý proces má podobnou stránku, kde můžete vybrat pozice prognózy. Na stránce **Přidat do pozic** se zobrazují všechny pozice prognózy, které jsou k dispozici pro výběr, zatímco na stránce **Aktualizovat pozice** se zobrazí pouze ty pozice prognózy, které již mají přiřazen prvek rozpočtových nákladů. (Stránka **Aktualizovat pozice** tak poskytuje způsob, jak zjistit, které prognózy pozice již mají připojený prvek nákladů.) Pozice prognózy můžete přesunout z horní mřížky do dolní a zahrnout je do aktualizace. 

Všimněte si, že funkce **Změnit data** na kartě **Výpočtu nákladů** okamžitě změní počáteční a koncové datum pro prvek rozpočtových nákladů v pozicích prognózy. Nejsou k dispozici žádné možností výběru. 

Na stránce **Skupina kompenzací** použije funkce **Aktualizace sazeb pozice** aktuální tabulku sazby kompenzace pro pozice prognózy, které jsou přiřazeny do skupiny. Sazby se aktualizují a další řádky prvku nákladů jsou přidány pro nové řádky v tabulce sazeb (na základě dat). Prvky rozpočtových nákladů a data zvýšení však nebudou aktualizována. Můžete vybrat, který proces plánování rozpočtu a scénář plánu rozpočtu chcete aktualizovat. Můžete tedy aktualizovat jeden scénář, ale ponechat jiný scénář pro porovnání nezměněn. 

Pokud vyberete pozice prognóz a klepnete na **Hromadná aktualizace**, můžete přidat nebo změnit zároveň více než jednu pozici prognózy. K dispozici je řada možností. Jedna možnost na kartě **Finanční dimenze** se mírně liší od ostatních a souvisí s prvky rozpočtových nákladů. Prvky rozpočtových nákladů můžete přidat nastavením možnosti **Výchozí hodnoty rozpočtu** na **Ano**. Pokud nejsou vybrány žádné prvky rozpočtových nákladů, ale **Výchozí hodnoty rozpočtu** jsou nastaveny na hodnotu **Ano**, budou odebrány všechny prvky rozpočtových nákladů, které jsou aktuálně přiřazeny. 

Proces přepočtu je automaticky použit pro všechny pozice prognózy, které se změnily.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Uvedení pozic prognózy do plánů rozpočtu

[![graphic6](./media/graphic6-1024x327.png)](./media/graphic6.png)

Účelem vytváření a úpravy pozic prognózy je jejich přidání k plánům rozpočtu tak, aby plány rozpočtu zahrnovaly nejaktuálnější částky rozpočtu. Existují dvě metody přidání pozic prognózy k plánům rozpočtu. Můžete použít proces generování nebo proces výběru pro plán rozpočtu.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Generování plánu rozpočtu z pozic prognózy

Funkce **Generovat plán rozpočtu z pozic prognózy** vytvoří nebo aktualizuje plány rozpočtu tak, aby měly částky rozpočtu a hodnoty FTE z pozic prognózy. Částky rozpočtu z pozice prognózy se stanou částkami na řádku plánu rozpočtu a jsou seskupeny podle hodnot finančních dimenzí a data platnosti. Proces generování přiřadí zdrojovou pozici prognózy k řádku plánu rozpočtu. Pokud chcete zobrazit pozici, můžete přidat pozici prognózy jako řádek v rozvržení pro plán rozpočtu, nebo použít dotaz **Řádky plánu rozpočtu**. Chcete-li přeskočit přiřazení, nastavte možnost **Zahrnout pozici v řádku plánu rozpočtu** na **Ne**. 

Můžete vybrat scénář FTE plánu rozpočtu počtu a zahrnou počet FTE v plánu rozpočtu. Vybírat lze pouze scénáře typu množství, které jsou zahrnuty v rozvržení cílového plánu rozpočtu. Když vyberete scénář FTE, je také nutné určit hlavní účet FTE. Tento účet se používá k vytvoření řádků plánu rozpočtu množství. 

Proces plánování rozpočtu a scénář plánu rozpočtu, které jsou vybrané ve zdroji, určují proces plánování rozpočtu cílového scénáře a scénář. Vzhledem k tomu, že tyto atributy jsou přiřazeny k pozicím prognózy, musí být synchronizovány a plánem rozpočtu. Atributy proto nemohou být upraveny v cíli. 

Podobně jako u dalších procesů generování jsou k dispozici tři možnosti:

-   **Vytvořit nový plán rozpočtu** – vytvoření nového plánu s atributy, které jsou vybrány v části **Cíl**.
-   **Nahradit existující scénář plánu rozpočtu** – odstranění všech dat v cílovém plánu rozpočtu ve vybraném scénáři plánu rozpočtu a vytvoření nových řádků, které mají vybraná data pozice prognózy.
-   **Aktualizovat existující scénář plánu rozpočtu a připojit nová data** – aktualizace existujících řádků v cílovém plánu, které odpovídají původním řádkům, a také přidání nových řádků pro nová data. Srovnání vychází z účtu hlavní knihy, dat, třídy rozpočtu a dalších hodnot, jako je například pozice prognózy. Všechny řádky, které mají číslo pozice odpovídající číslu zdrojové pozice, budou nahrazeny novými řádky ze zdroje.

### <a name="selecting-forecast-positions"></a>Výběr pozic prognózy

Můžete také přiřadit částky rozpočtu pro pozici prognózy přímo do plánu rozpočtu. Pomocí funkce **Přidat pozice** nad řádky plánu rozpočtu můžete vybrat pozice prognózy, které chcete zahrnout. 

Scénáře plánu rozpočtu, které lze vybrat jako zdroj, jsou omezeny na scénáře, které jsou zahrnuty v rozvržení plánu. Jedna možnost na kartě **Cíl** slouží k určení toho, že scénář FTE a hlavní účet mohou zahrnout počty FTE, ale není to vyžadováno. 

Tento proces výběru se chová jako možnost **Aktualizovat existující scénář plánu rozpočtu a připojit nová data** pro proces generování. Všechny stávající řádky plánu rozpočtu, kde je pozice prognózy přidána, jsou odebrány a nahrazeny novými řádky založenými na aktuálním stavu pozice prognózy.

#### <a name="date-options"></a>Možnosti data

Pro proces generování i proces výběru určuje počáteční datum na řádku prvku rozpočtových nákladů datum platnosti odpovídajícího řádku plánu rozpočtu. Pole **Metoda přidělení** na stránce s nastavením prvku rozpočtových nákladů určuje metodu přidělení:

-   **Počáteční datum** – počáteční datum prvku rozpočtových nákladů bude použito jako datum platnosti řádku plánu rozpočtu.
-   **Měsíční** – částka rozpočtu je rovnoměrně rozdělena počtem měsíců v časovém období pro vytvoření typické měsíční částky přiřazené k prvnímu dni každého měsíce. Pokud je první období částečným měsícem, částka pro daný měsíc bude vynásobena počtem dnů, kdy jsou náklady aktivní v daném měsíci, a výsledek je přiřazen k počátečnímu datu. Částka pro poslední měsíc je rozdílem celkové částky rozpočtu a součtu všech dalších měsíců. Proto zaokrouhlení může ovlivnit částku za poslední měsíc.
-   **Čtvrtletní** – tato metoda je stejná jako **Měsíční**, ale výpočty se provádí pro tříměsíční období.
-   **Týdenní** – logika se podobá logice metodě **Měsíční** a **Čtvrtletní**. Částka rozpočtu je rovnoměrně rozdělena počtem týdnů v časovém období pro vytvoření typické týdenní částky přiřazené k prvnímu dni každého týdnu. Pokud je první období částečným týdnem, částka pro daný týden bude vynásobena počtem dnů, kdy jsou náklady aktivní v daném týdnu, a výsledek je přiřazen k počátečnímu datu. Částka pro poslední týden je rozdílem celkové částky rozpočtu a součtu všech dalších týdnů. Proto zaokrouhlení může ovlivnit částku za poslední týden.
-   **Každé 2 týdny** – tato metoda je stejná jako **Týdenní**, ale výpočty se provádí pro období 2 týdnů.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Změna řádků plánu rozpočtu, které mají pozice prognózy

Řádky plánu rozpočtu popisují zdroj částek rozpočtu (číslo pozice prognózy), ale nejsou propojeny. Proto změny v pozici prognózy se nezobrazují na řádku plánu rozpočtu, a změny na řádku plánu rozpočtu jsou zobrazeny v pozici prognózy. Pokud změníte pozici prognózy a chcete, aby aktualizace byly zahrnuty do plánu rozpočtu, je nutné znovu přenést pozici prognózy do plánu. Nezapomeňte však, že tento proces odebere všechny řádky, kterým je přiřazena tato pozice prognózy. Z tohoto důvodu všechny změny provedené v těchto řádcích budou odebrány. 

Pokud chcete zobrazit, do kterých plánů rozpočtu byly zahrnuty pozice prognózy, lze vygenerovat hlášení **Pozice prognózy podle plánu rozpočtu**. U pozice prognózy případně můžete otevřít okno s fakty **Přidružené plány rozpočtu** a zobrazit plány.




