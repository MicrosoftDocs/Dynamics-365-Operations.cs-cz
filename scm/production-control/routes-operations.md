---
title: "Postupů a operací"
description: "Toto téma obsahuje informace o postupech a operacích. Trasa definuje proces pro výrobu produktu nebo varianty produktu. Popisuje jednotlivé kroky (operace) ve výrobním procesu a tyto kroky musíte provést v uvedeném pořadí. Pro každý krok trasa také definuje požadované operace prostředky, čas požadované nastavení a běhu a výpočet nákladů."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Postupů a operací

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o postupech a operacích. Trasa definuje proces pro výrobu produktu nebo varianty produktu. Popisuje jednotlivé kroky (operace) ve výrobním procesu a tyto kroky musíte provést v uvedeném pořadí. Pro každý krok trasa také definuje požadované operace prostředky, čas požadované nastavení a běhu a výpočet nákladů.

<a name="overview"></a>Přehled
--------

Trasa popisuje pořadí operace potřebné k výrobě produktu nebo varianty produktu. Pro každou operaci postupu také definuje operace prostředky, které jsou požadovány, čas, který je nutný pro nastavení a provádění operace a výpočet nákladů. Můžete použít stejný postup k vytvoření více produktů nebo můžete definovat jedinečný postup pro každý produkt nebo varianta produktu. Můžete mít i více tras pro stejný produkt. V tomto případě postup, který se používá se liší v závislosti na faktorech, jako je množství, které je třeba vyrobit. Definici trasy v 365 Microsoft Dynamics pro operace se skládá ze čtyř samostatných prvků, které společně popisují proces výroby:

-   **Trasa** – trasa definuje strukturu výrobního procesu. Jinými slovy určuje pořadí operací.
-   **Operace** – operaci identifikuje pojmenované kroku v postupu, jako například **sestavení**. Stejné operace může dojít v několika trasami a může obsahovat čísla různých operací.
-   **Vztah operací** – vztah operace definuje provozní vlastnosti operace, například čas instalace a běhu, nákladových kategorií, parametry spotřeby a požadavky na zdroje. Vztah operací umožňuje provozní vlastnosti operace se liší podle použitého v operaci postupu nebo produktů, které jsou vyráběné.
-   **Verze postupu** – verze postupu definuje trasu, která se používá k výrobě produktu nebo varianty produktu. Verze postupu povolit cesty k opětovné použití mezi produkty nebo změněna v průběhu času. Umožňují také různé trasy má být použit k výrobě stejného výrobku. Trasu, která se používá v tomto případě závisí na faktorech, jako je umístění nebo množství, které je třeba vyrobit.

## <a name="routes"></a>Postupy
Trasa popisuje pořadí operací, který se používá k výrobě produktu nebo varianty produktu. Každá operace je přiřazeno číslo operace a následné operace. Pořadí operací vytváří síť tras, která může být reprezentováno pomocí řízené grafu, který má jeden nebo více počátečních bodů a jeden koncový bod. V 365 Dynamics pro operace se rozlišují podle typu konstrukce tras. Jsou dva typy tras, jednoduché trasy a trasy sítí. V parametry modulu řízení výroby můžete určit, zda lze použít pouze jednoduché trasy nebo zda lze použít složitější trasy sítí.

### <a name="simple-routes"></a>Jednoduché cesty

Jednoduchý postup je sekvenční a existuje pouze jeden počáteční bod trasy.  

[![Jednoduchý postup](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Pokud povolíte pouze jednoduché trasy v parametry modulu řízení výroby, 365 Dynamics pro operace automaticky generuje čísla operace (10, 20, 30 a tak dále) při definování postupu.

### <a name="route-networks"></a>Směrování sítě

Pokud povolíte složitější trasy sítí v parametry modulu řízení výroby, můžete definovat trasy, které mají více počátečních bodů a operace, které lze spustit současně.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Poznámky:**

-   Každou operaci může mít pouze jeden následník operace a celá cesta musí končit v jediné operaci.
-   Neexistuje žádná záruka, že více operací, které mají stejnou operaci následníka (například operace 30 a 40 na předchozím obrázku) skutečně probíhat souběžně. Omezení tak, že operace budou naplánovány ukládat dostupnosti a kapacity zdrojů.
-   Jako číslo operace nelze použít hodnotu 0 (nula). Toto číslo je vyhrazen a slouží k určení, zda poslední operaci v postupu má žádné následné operace.

### <a name="parallel-operations"></a>Paralelní operace

Kombinace více zdrojů operací, které mají odlišné vlastnosti někdy je vyžadován k provedení operace. Montáž může například vyžadovat, stroje, nástroje a jednoho pracovníka na každých dvou strojů dohlížet operaci. V tomto příkladu lze modelovat pomocí paralelní operace, kde jedna operace je určen jako primární operace a ostatní jsou sekundární.  

[![Cestu, která má primární a sekundární operace.](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Primární operace obvykle představuje kritický prostředek a určí běhu pro sekundární operace. Však během plánování, který zahrnuje omezenou kapacitu, prostředky, které jsou naplánovány pro operace primární a sekundární operace musí být k dispozici a mají volné kapacity současně.  

Operace primární a sekundární operace musí mít stejné číslo operace (30 na předchozím obrázku).  

V předchozím příkladu je požadavek na prostředek pro primární operace (30) počítače, že jsou požadavky na zdroje pro sekundární operace (30' a 30'') nástroj a pracovníka. 50 % vytížení pomáhá zajistit, aby plánované pracovní můžete dohlížet dvou strojů současně.

### <a name="approval-of-routes"></a>Schválení postupů

Trasa musí být schválen dříve, než jej lze použít v procesu plánování a výroby. Schválení znamená, že byl dokončen návrh trasy. Stejný produkt uvolněn nebo uvolněný produkt varianty může mít více schválených postupů. Schválení postupu obvykle vyvolá se při první verze odpovídající postupu schválena. Však v některých obchodních scénářů, schválení postupu a verze postupu jsou samostatné aktivity, které může zahrnovat proces různých vlastníků.  

Každá trasa může být schválené a neschválené samostatně. Uvědomte si však, aby při neschválené trasy související verte se také Neschváleno. V parametry modulu řízení výroby lze určit, zda trasy mohou neschválené a zda je možné změnit schválených postupů.  

Že záznamy, kteří schválí všechny trasy musí uchovávat záznam, můžete požadovat elektronických podpisů schválení postupu. Uživatelům bude muset potvrdit svou identitu pomocí [elektronický podpis](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Operace
Operace je krok ve výrobním procesu. V 365 Dynamics pro operace každá operace má ID a jednoduchý popis. Následující tabulka ukazuje typické příklady operací z dílny strojní.

| Operace  | popis        |
|------------|--------------------|
| PipeCut    | Řezání potrubí       |
| TIGweld    | TIG svařování        |
| JigAssy    | Jig sestavení       |
| Kontrola | Kontrolu kvality |

Provozní vlastnosti operace, jako je například doba seřízení a běhu, požadavky na zdroje, informace o ocenění a výpočet spotřeby jsou určeny na vztah operace. (Další informace o vztazích naleznete v další části.)

## <a name="operation-relations"></a>Vztahy operací
Následující provozní vlastnosti operace jsou udržovány na vztah operace:

-   Nákladové kategorie
-   Parametry spotřeby
-   Časy zpracování
-   Zpracování množství
-   Požadavky na prostředek
-   Poznámky a pokyny

Můžete definovat více relace operací pro stejné operace. Nicméně každý vztah operace je specifický pro jednu operaci a obsahuje vlastnosti, které jsou specifické pro trasu, uvolněný produkt nebo sadu uvolněné produkty, které se vztahují na skupinu položek. Tedy stejné operace lze více tras, které mají různé provozní vlastnosti. Navíc můžete snadněji Udržovat hlavní data při použití standardních operací, které mají stejné provozní vlastnosti, bez ohledu na trasu, která se používá a produkt, který je vytvořen. Působnosti vztah operace je definována prostřednictvím **kód položky**, **vztahu položky**, **kód postupu** a **směrování vztah** vlastnosti, jak je znázorněno v následující tabulce.

| Kód položky | Vztah položky         | Kód postupu | Vztah postupu   | Rozsah vztah operace                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabulka     | &lt;ID položky&gt;       | Postup      | &lt;ID postupu&gt; | Provozní vlastnosti operace, pokud je použit v postupu kde **číslo postupu**=&lt;ID postupu&gt; uvolněný produkt vyrábět kde **číslo položky**=&lt;ID položky&gt;.                                                                                                                        |
| Tabulka     | &lt;ID položky&gt;       | Vše        |                  | Výchozí provozní vlastnosti operace se používá k výrobě uvolněný produkt kde **číslo položky**=&lt;ID položky&gt;. Jinými slovy tyto provozní vlastnosti použít, pokud neexistuje žádný vztah operace postupu specifické pro uvolněný produkt.                                     |
| Seskupit     | &lt;ID skupiny zboží&gt; | Postup      | &lt;ID postupu&gt; | Provozní vlastnosti operace, pokud je použit v postupu kde **číslo postupu**=&lt;ID postupu&gt; pro vytvoření uvolněné produkty, které jsou přidruženy skupiny položek &lt;položky ID skupiny&gt;, pokud neexistuje vztah operace postupu specifické pro uvolněný produkt.                         |
| Seskupit     | &lt;ID skupiny zboží&gt; | Vše        |                  | Výchozí provozní vlastnosti operace se používá k vytvoření uvolněné produkty, které jsou přidruženy skupiny položek &lt;položky ID skupiny&gt;, pokud existuje zvláštní vztah operací.                                                                                                  |
| Vše       |                       | Postup      | &lt;ID postupu&gt; | Výchozí provozní vlastnosti operace, pokud je použit v postupu kde **číslo postupu**=&lt;ID postupu&gt;. Jinými slovy tyto provozní vlastnosti použít v případě, že neexistuje žádný vztah operace této trasy, který je specifický pro buď uvolněný produkt nebo má přiřazeny skupiny položek. |
| Vše       |                       | Vše        |                  | Výchozí provozní vlastnosti operace. Tyto provozní vlastnosti použít, pokud neexistuje zvláštní vztah operací.                                                                                                                                                                |

Můžete také určit, zda je vztah operace specifické pro web. Tímto způsobem lze provozní vlastnosti operace závisí na umístění (to znamená, web), pokud je operace provedena. Pro konfigurované výrobky můžete také určit různé provozní vlastnosti pro každou konfiguraci produktu.  

Operce poskytují velkou pružnost při definování vaší trasy. Schopnost definovat výchozí vlastnosti navíc pomáhá snížit množství hlavních dat, která musí udržovat. Tato flexibilita však také znamená, že musíte být vědomi, změnit vztah operace v kontextu.  

**Poznámka:** provozní vlastnosti jsou uloženy ve vztazích operace na operaci na trase, všechny výskyty stejné operace (například sestavení) mají stejnou dobu instalace, spuštění, požadavky na zdroje atd. Proto pokud dva výskyty operaci musí dojít ve stejné trase, ale mají různou dobu běhu, je nutné vytvořit dvě samostatné operace, například Assembly1 a Assembly2.

### <a name="modifying-product-specific-routes"></a>Změna trasy konkrétní produkt

Při otevření **postupu** stránky z **vydala podrobnosti o produktu** stránky, jsou uvedeny verze postupu, které jsou přidruženy k vybranému produktu vydané. V tomto kontextu pro každou operaci 365 Dynamics pro operace ukazuje provozní vlastnosti z vztah operace, aby co nejlépe odpovídalo verze postupu. Zjistíte, že obsahuje seznam operací **kód položky** a **kód postupu** vlastnosti z vztah operace. Proto lze určit, který vztah operace je zobrazen.  

Na **postupu** stránky, můžete změnit provozní vlastnosti operace, například době běhu nebo nákladových kategorií. Provedené změny jsou uloženy na vztah operace, který je specifický pro trasy a uvolněný produkt, který se odkazuje v aktuální verze postupu. Není-li vztah operace, který se zobrazuje konkrétní trasy a uvolněný produkt před jsou uloženy změny, systém vytvoří kopii vztah operace. Tato kopie *je* konkrétní trasy a uvolněný produkt. Proto změny neovlivní jiné trasy nebo uvolněných produktů. Chcete-li ověřit, který vztah operace se upravuje na **postupu** stránky, podívejte se na **kód položky** a **kód postupu** pole.  

Můžete také ručně vytvořit operaci, která je pomocí zvláštních postupů a uvolněný produkt **kopírovat a upravit vztah** funkce.  

**Poznámka:** na novou operaci postupu přidáte **postupu**, vztah operace vytvoření stránky pouze pro aktuální uvolněný produkt. Proto pokud trasa slouží také k výrobě jiných uvolněné produkty, bude existovat žádný vztah operace použitelná pro tyto produkty vydané a trasu lze použít již pro uvolněné produkty.

### <a name="maintaining-operation-relations-per-route"></a>Udržování vztahů operací na trase

Při otevření **podrobností o postupu** ze stránek **trasy** stránku seznamu je zobrazen seznam všech vztahů operací, které platí pro vybranou trasu. Proto lze snadno ověřit, provozní vlastnosti, které se používají pro produkty. Můžete upravit výchozí hodnoty vlastností a hodnot vlastností specifické pro daný produkt.  

Pokud přidáte nový vztah operace na **podrobností o postupu** stránky, **kód postupu** je automaticky nastaveno na **postupu**a **směrování vztah** pole je nastavena na číslo postupu aktuální trasy.

### <a name="maintaining-operation-relations-per-operation"></a>Udržováním vztahů operace na operaci

Z **operace** můžete otevřít stránku, **vztahů operací** stránky. Na této stránce můžete upravit všechny relace operací pro určité operace. Dokonce můžete upravit vztahy operací, které obsahují výchozí hodnoty.  

Pokud váš podnik používá standardní operace a provozní parametry jsou stejné ve všech produktů a procesů, **vztahů operací** stránka poskytuje pohodlný způsob, jak spravovat výchozí provozní vlastnosti těchto operací.

### <a name="applying-operation-relations"></a>Použití vztahů operací

V některých případech nutné 365 Dynamics pro operace najít provozní vlastnosti operace. Například při vytvoření nákupní objednávky, provozní vlastnosti každé operace musí být zkopírovány z vztahů operací do výrobního postupu. V těchto situacích 365 Dynamics pro operace vyhledá příslušné operace vztahy od nejvíce specifické kombinaci alespoň určitou kombinaci.  

Při 365 Dynamics pro operace vyhledávání nejrelevantnější vztah operace pro uvolněný produkt, operace vztah, který odpovídá ID položky pro uvolněný produkt je upřednostňováno prostřednictvím vztahu operací že odpovídá skupině položky ID. Operace vztah, který odpovídá ID položky skupiny je zase upřednostňována před výchozí vztah operace. Vyhledávání se provádí v následujícím pořadí:

1.  **Kód zboží**=**tabulka** a **vztahu položky**=&lt;ID položky&gt;
2.  **Kód zboží**=**skupiny** a **vztahu položky**=&lt;skupiny ID položky&gt;
3.  **Kód zboží**=**všechny**
4.  **Kód postupu**=**postupu** a **směrování vztah**=&lt;ID postupu&gt;
5.  **Kód postupu**=**všechny**
6.  **Konfigurace**=&lt;ID konfigurace&gt;
7.  **Configuration**=
8.  **Web**=&lt;ID webu&gt;
9.  **Site**=

Proto operace by měla sloužit pouze jednou pro každou trasu. Pokud operace dochází více než jednou ve stejné trase, všechny výskyty této operace bude mít stejný vztah operace a nebudete moci každý mají různé vlastnosti (například časy spuštění).

## <a name="route-versions"></a>Verze postupu
Verze postupu se používají k implementaci odlišností při výrobě výrobků nebo poskytnout větší kontrolu nad procesem výroby. Definují trasu, která by měla sloužit při vydání konkrétní produkt nebo varianta uvolněný produkt pochází. K definování postupu, který se používá pro uvolněný produkt, můžete použít následující omezení:

-   Rozměry výrobku (velikost, barvu, styl nebo konfigurace)
-   Výrobní množství
-   Výrobní závod
-   Datum výroby

Pokud jste výrobu produktu na konkrétním místě v předepsaném množství, nebo v určitém období, lze označit jako výchozí verze postupu specifické verze postupu. Uvědomte si však, že pouze jeden aktivní trasa je povolena pro daný produkt vydané a danou sadu omezení.  

V parametry modulu řízení výroby můžete zadat dobu platnosti verze postupu vždy požadovat.

### <a name="approval-of-route-versions"></a>Schválení verze postupu

Před použitím verze postupu plánování nebo výrobního procesu musí být schváleny. Když schválíte verzi postupu, můžete schválit také související trasy. Uvědomte si však, že pouze v případě, že je schválen také související trasy lze schválit verze postupu.

### <a name="activating-the-default-route-version"></a>Aktivace verze postupu výchozí

Při aktivaci verze postupu určíte jej bude používat verzi výchozí trasy, kterou hlavní plánování nebo které se budou používat k vytváření výrobních zakázek. Můžete mít pouze jeden aktivní verze postupu pro danou sadu omezení (například období, webu nebo množství). Pokud je verze, že se pokoušíte aktivovat konflikty verzí, který je již aktivní, obdržíte chybovou zprávu. Chcete-li zabránit dvojznačný aktivace, musíte pak deaktivovat konfliktní verze nebo upravit omezení (obvykle tečka) ve verzi postupu.

### <a name="electronic-signatures"></a>Elektronické podpisy

V případě, že záznamy, které schvaluje a aktivuje jednotlivé verze postupu musí uchovávat záznam, můžete požadovat elektronických podpisů pro tyto úkoly. Uživatelé, kteří schválit a aktivovat verze postupu bude muset potvrdit svou identitu pomocí [elektronický podpis](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Změna produktu, která používá Správa případů

Produktu změnit velikost písmen pro schválení a aktivace nových nebo změněných trasách a verze postupu poskytuje snadný způsob, jak zobrazit přehled omezení verze postupu. Můžete schválit a aktivovat všechny trasy, které souvisejí s určitou změnu v jedné operaci a dokumentovat výsledky v případu změny produktu.

## <a name="maintaining-routes"></a>Správa trasy
V závislosti na obchodní požadavky je možné ke snížení intenzity rybolovu, který je nutný pro udržení vaší definice procesu.

### <a name="making-routes-independent-of-resources"></a>Vytváření trasy nezávislých zdrojů

V mnoha systémech musí být určena operace zdroje nebo skupiny zdrojů, který by měl provést operaci v postupu. V 365 Dynamics pro operace, však můžete definovat sadu požadavků, které musí splňovat provozní prostředek se pro operaci. Proto určité operace zdroje nebo skupiny zdrojů, které má být použito nemusí stanovit, dokud je ve skutečnosti naplánované operace. Tato funkce je užitečná, pokud máte mnoho zaměstnanců nebo stroje, které můžete provést stejnou operaci.  

Například určíte, že vyžaduje-li operace operace prostředku **stroje** typ, který má **Stamping** schopnost 20 tun. Plánovací modul pak vyřeší tyto požadavky na specifické operace zdroje nebo skupiny zdrojů při plánování operace. Vzhledem k tomu, že je možné zadat pouze tyto požadavky namísto operace vazby na konkrétní počítač, máte mnohem větší flexibilitu. Údržba je navíc snazší při přesunu zdrojů nebo jsou přidány nové zdroje.  

Další informace o různých typech požadavků na zdroje a jejich použití naleznete v tématu požadavky na zdroje operace a [schopnosti prostředku](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Sdílení tras na webech

Vyrobit stejný produkt na více než jednom produkčním a kroky k výrobě produktu jsou že stejné ve všech místech, můžete navrhnout často sdílené cesty, která se používá na všech serverech výroby. K vytvoření sdílené cesty, není zadejte na trati sám. Musí však stále vytvořit verzi postupu, který přidruží sdílenou trasu produktu v každém místě.  

Musíte také zkontrolovat, že nemůžete volat pro určité operace zdroje nebo skupiny zdrojů požadavky na zdroje pro každou operaci v postupu, ale místo vyjádřená charakteristiky požadované prostředky. Pak bude možné přiřadit prostředky odpovídající operace z webu, který výroba je naplánována na plánovací modul. Například pokud existují malé rozdíly v době běhu nebo je čas nastavení pro konkrétní operaci pro danou lokalitu, můžete použít tyto informace přidáním vztahu další operací pro daný web.  

Chcete-li plně využít výhod sdílené cesty, také používejte spotřebu zdrojů na odpovídající kusovník (BOM). Pokud nastavíte příznak pro spotřebu prostředků na řádku Kusovníku, sklad a umístění, které suroviny by měl být používán z je odvozeno z zdroj operace, operace je naplánována na. Proto skladu a umístění není nutné stanovit, dokud skutečně plánování výroby se. Tímto způsobem můžete vytvořit Kusovník a postup nezávislé na fyzické umístění, kde je produkt vyroben.

### <a name="standard-operation-relations"></a>Standardní operace vztahy

Pokud váš podnik používá standardizovaný operací v průběhu výroby a je velmi málo nebo žádné kolísání doby seřízení, běhu, výpočet spotřeby, výpočet, nákladů a atd., může být vhodné vytvoření výchozí relace operací pro všechny operace. V tomto případě Nevytvářejte relace operací, které jsou specifické pro všechny trasy nebo vydání produktu.  

Pokud také express prostředku požadavky na dovednosti a schopnosti a vytvořit nezávislý na webu vaší trasy, pomáhá zachovat minimální průběžnou údržbu firemních procesů.  

Pokud použijete tento přístup **vztahů operací** stránka se stane vaší primární cíl zachování doby běhu a další vlastnosti.

### <a name="resource-specific-process-times"></a>Časy zpracování specifických prostředků

Pokud nezadáte operace zdroje nebo skupiny zdrojů v rámci požadavky na zdroje pro operaci, použitelné prostředky může pracovat při různých rychlostech. Proto se může lišit čas, která je požadována pro zpracování operace. Chcete-li tento problém vyřešit, můžete použít **vzorec** na vztah operací určete způsob výpočtu času zpracování. Existují tyto možnosti:

-   **Standardní** – (výchozí možnost) výpočet používá pouze pole z vztah operace a násobí množství objednávky zadané běhu.
-   **Kapacita** – zahrnuje výpočet **kapacity** z prostředku operací. Čas je tedy závislé na prostředku. Hodnota uvedená na provozní prostředek je Hodinová kapacita. Tato hodnota je vynásobena číslem množství na objednávce a **faktor** hodnotu z vztah operace.
-   **Dávky** – kapacita dávky se počítá s použitím informací ze vztah operace. Počet listů a tím i čas zpracování lze pak vypočte na základě množství objednávky.
-   **Dávka prostředku** – tato možnost je v podstatě stejný jako **listu** možnost. Však obsahuje výpočet **dávky kapacity** z prostředku operací. Čas je tedy závislé na prostředku.


<a name="see-also"></a>Viz také
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)




