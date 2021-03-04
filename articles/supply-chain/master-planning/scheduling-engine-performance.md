---
title: Zlepšení výkonu plánovacího modulu
description: Toto téma poskytuje informace o plánovacím modulu a o tom, jak zlepšit výkon.
author: ChristianRytt
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c1b940754021956998fe27ba16020d4b16aedf1
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424126"
---
# <a name="improve-scheduling-engine-performance"></a>Zlepšení výkonu plánovacího modulu

[!include [banner](../includes/banner.md)]

Modul pro plánování zdrojů se používá při plánování tras pro plánované a vydané výrobní zakázky. Modul byl původně vydán jako součást Dynamics AX 2012 a od svého vydání prošel několika vylepšeními.

[Plánování úloh v dílně](https://en.wikipedia.org/wiki/Job_shop_scheduling) je extrémně složitý kombinatorický problém, u něhož čas řešení exponenciálně roste s počtem rozhodovacích proměnných. Zákazníci často nastavují výrobní trasy a související data způsobem, který vede k problému s plánováním, který nelze vyřešit v rozumném čase ani na nejmodernějším hardwaru. Toto téma vám pomůže pochopit plánovací modul a jaký vliv může mít konkrétní nastavení na výkon.

Pokud jde o zlepšení výkonu plánování, obecné pokyny doporučují snížit složitost problému, který musí modul vyřešit. Mezi hlavní faktory, které můžou ovlivnit výkon, patří:

- Trasy s mnoha operacemi
- Trasy s paralelními operacemi
- Operace s počtem zdrojů vyšším než jeden
- Operace s mnoha použitelnými zdroji
- Používání pevných odkazů
- Používání omezené kapacity
- Počet různých kalendářů, které se používají
- Počet slotů pracovní doby za den v kalendáři
- Celková doba trvání trasy
- Paralelní spuštění více plánovacích modulů

## <a name="overview-of-basic-scheduling-flow"></a>Přehled základního toku plánování

Abychom porozuměli, jak může dané nastavení ovlivnit výkon, je důležité v určité základní míře pochopit tok tohoto procesu, a to jak uvnitř modulu, tak v kódu X++, který ho obklopuje.

Základní proces plánování zakázky se skládá ze tří hlavních kroků:

- **Načítání dat** – Zde jsou datové modely X++ transformovány do interního datového modelu pro modul ve formě úloh a omezení.
- **Plánování** – Toto je hlavní zdroj pro plánování, který zpracovává daný model a omezení a pak generuje výsledek. Během tohoto procesu bude modul podle potřeby požadovat informace o pracovní době a stávající ch rezervacích kapacity z X++.
- **Ukládání dat** – Výsledek modulu ve formě slotů pro rezervaci kapacity úloh je zpracován kódem X++, aby se rezervace kapacity uložily a aby se aktualizovaly časy zahájení a ukončení úloh/operací/zakázek.

## <a name="load-data-into-the-engine"></a>Načítání dat do modulu

Plánovací modul má abstraktnější datový model než databáze Supply Chain Management, protože byl vytvořen jako obecný modul, který dokáže zpracovat různé zdroje dat. Koncepty trasy, sekundární operace a doby běhu je třeba „přeložit“ do obecného modelu úlohy a omezení, který modul vystavuje. Logika pro sestavení modelu zahrnuje značné množství obchodní logiky a liší se v závislosti na zdrojových datech. Odpovědnou třídou X++ je `WrkCtrScheduler` a pak tu jsou odvozené třídy pro plánované výrobní zakázky, uvolněné výrobní zakázky a prognózy projektů.

Jako příklad si představme trasu uvedenou v následující tabulce a na následujícím obrázku, která se zdá být relativně jednoduchá.

| Číslo operace | Priorita | Přípravný čas | Operační čas | Čas čekání po oper. | Množství prostředků | Další |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Primární | 1.00 | 2.00 | | 1 | 20 |
| 10 | Sekundární&nbsp;1 | | | | 1 | 20 |
| 20 | Primární | | 3.00 | 1.00 | 3 | 0 |

![Příklad schématu trasy](media/scheduling-engine-route.png "Příklad schématu trasy")

Při odesílání do modulu dojde k rozdělení do 8 úloh, jak je znázorněno na následujícím obrázku (vyberte obrázek pro jeho zvětšení).

[![Úlohy plánovacího modulu](media/scheduling-engine-jobs.png "Úlohy plánovacího modulu")](media/scheduling-engine-jobs-large.png)

Standardní propojení mezi dvěma úlohami je `FinishStart`, což znamená, že čas ukončení jedné úlohy musí být před časem zahájení jiné úlohy. Protože nastavení musí být provedeno stejným zdrojem, který tento proces později provede, existují mezi nimi omezení `OnSameResource`. Mezi úlohami pro primární a sekundární operaci 10 existují propojení `StartStart` a `FinishFinish`, což znamená, že úlohy musí začínat i končit současně, a zároveň platí omezení `NotOnSameResource`, která zabrání spuštění stejného zdroje pro primární i sekundární operaci.

Pro operaci 20, kde bylo množství zdrojů nastaveno na 3, byla procesní úloha rozdělena do 3 odlišných úloh, které musí všechny běžet ve stejnou dobu.
V tomto případě byla skupina tras nastavena tak, aby po určitých intervalech nerezervovala kapacitu pro frontu, a proto po ní existuje pouze jedna úloha.

Plánovací modul rozumí pouze konceptu úloh a nemá žádnou představu o operacích. To znamená, že při plánování jsou operace také rozděleny na úlohy, i když v databázi nebudou trvalé.

U každé úlohy také definujeme určitý požadavek na kapacitu úlohy (požadovaný počet sekund). V závislosti na tom, jak byly definovány požadavky na zdroje, můžeme také pro každou úlohu odeslat seznam všech potenciálních použitelných zdrojů, které by úloha mohla využít, a jaké jsou požadavky na kapacitu pro jednotlivé zdroje. I když se seznam použitelných zdrojů odesílá při vytváření modelu, modul bude muset i tak zajistit, aby přiřazení prostředků bylo skutečně platné po celou dobu trvání úlohy.

## <a name="scheduling-engine-internals"></a>Vnitřní části plánovacího modulu

### <a name="scheduling-engine-interface"></a>Rozhraní plánovacího modulu

Chcete-li získat představu o tom, jak modul funguje interně, je nejlepší podívat se na funkčnost, kterou externě vystavuje. Hlavním rozhraním v X++ je `WrkCtrSchedulerEngineInterface`. Zahrnuje metody popsané v následujících pododdílech.

#### <a name="general-engine"></a>Obecný modul

| **Metoda** | **Účel** |
| --- | --- |
| `run` | Plánuje všechny načtené úlohy a vrací kód chyby. |
| `getJobSchedulingSequenceResult` | Získá výsledek plánování a první chybovou úlohu v sekvenci identifikované konkrétní úlohou. |
| `validateJobCapacityReservations` | Ověří rezervace kapacity pro všechny úlohy uložené modulem. |
| `setReservationsTimeStamp` | Odešle časové razítko do sady modulu u všech nových rezervací kapacity pro naplánované úlohy v mezipaměti modulu. |
| `addPropertyToGroupAggregation` | Přidá předponu vlastnosti do sady vlastností použité při agregaci kapacity. |
| `addResource` | Přidá zdroj do fondu zdrojů plánovacího modulu. |
| `addResourceGroup` | Přidá skupinu zdrojů do fondu skupin zdrojů plánovacího modulu. |
| `addResourceGroupMembership` | Přidá zdroj jako člen do skupiny zdrojů. |
| `addOptimizationGoal` | Přidá cíl optimalizace plánování (doba trvání nebo priorita). |

#### <a name="individual-jobs"></a>Jednotlivé úlohy

| **Metoda** | **Účel** |
| --- | --- |
| `addJobInfo` | Přidá záznam s informacemi o úloze, který informuje modul o úloze, která by měla být naplánována. |
| `addConstraintJobEndsAt` | Přidá omezení, že by úloha měla skončit k určitému datu a v určitém čase. |
| `addConstraintJobStartsAt` | Přidá omezení, že by úloha měla začít k určitému datu a v určitém čase. |
| `addConstraintMaxJobDays` | Definuje omezení, že se může úloha může protáhnout na zadaný maximální počet dní. |
| `addConstraintResourceRequirement` | Přidá omezení, že úloha musí být naplánována na konkrétním zdroji. |
| `addJobBindPriority` | Přidá prioritu propojení úlohy pro pár (úloha, úroveň omezení). Vyšší hodnota priority znamená, že proměnné úlohy budou propojeny dříve. Úloha bude zpracována před úlohami s nižší prioritou ve stejné posloupnosti. |
| `addJobCapacity` | Přidá informace o vytížení kapacity u úlohy (například požadovaná doba běhu úlohy) – bez ohledu na to, na kterém zdroji úloha běží. |
| `addJobResourceCapacity` | Přidá zdroj do sady zdrojů, které lze použít k provedení úlohy, a uvádí požadovanou kapacitu při spuštění na tomto zdroji. |
| `addJobGoal` | Přidá informace o cíli úlohy pro konkrétní úroveň omezení (nejdřívější čas dokončení nebo nejzazší čas zahájení). |
| `addJobResourcePriority` | Přidá prioritu, která se má použít, když je úloha naplánována na zdroji. |
| `addJobResourceRuntime` | Určuje čas úlohy, který je závislý na zdroji, na kterém bude úloha naplánována. |
| `addJobRuntime` | Určuje čas úlohy, který je nezávislý na zdroji, na kterém bude úloha naplánována. |
| `scheduleJobOnResourceGroup` | Označí úlohu pro plánování na úrovni skupiny zdrojů. |
| `setJobResourcePreemptionAllowed` | Určuje, zda je povolena preference pro úlohu u zdroje (pokud je modulu povoleno naplánovat úlohu v nenavazujících kapacitních slotech). |
| `setRequiredNumberOfResources` | Nastaví počet zdrojů potřebných k naplánování úlohy (jen pro plánování operací). |

#### <a name="constraints-between-jobs"></a>Omezení mezi úlohami

| **Metoda** | **Účel** |
| --- | --- |
| `addJobLink` | Přidá propojení (například finish\>start) mezi dvěma úlohami. |
| `addConstraintEndsDelayed` | Definuje omezení, že úloha nemůže skončit před dokončením jiné úlohy (plus nějaká doba zpoždění). |
| `addConstraintJobListWorkingTimeIntersect` | Přidá omezení, že se kapacitní sloty rezervované pro úlohy musí nacházet v překrývající se pracovní době obou zdrojů používaných úlohami. |
| `addConstraintJobOverlap` | Přidá omezení, které definuje posloupnost úloh, když lze dané množství položky přesouvat mezi dvěma zdroji v době, kdy první zdroj stále není dokončen – aby mohl druhý zdroj začít se zpracováním. |
| `addConstraintNotOnSameResource` | Přidá omezení, že by dvě úlohy neměly být naplánovány na stejném zdroji. |
| `addConstraintOnSameResource` | Přidá omezení, že dvě úlohy musí být naplánovány na stejném zdroji. |
| `addJobSameReservations` | Přidá omezení, že úloha musí nakonec mít rezervace kapacity pro stejné časové sloty jako primární úloha. |
| `setPrimaryParallelJob` | Přidá informaci o tom, která úloha je primární v sadě paralelních úloh. |

### <a name="solver"></a>Řešitel

Samotný modul je v podstatě specializovaný řešitel omezení s přidanou vlastní heuristikou. Tento řešitel je založen na dvou hlavních prvcích: proměnných a omezeních.

#### <a name="variable"></a>Proměnná

Proměnná představuje sadu možných hodnot. Plánovací modul má dva typy proměnných:

- **Proměnná DateTime** – Zahrnuje sadu všech dat a časů a dá se omezit přesunutím dolní a horní hranice pro čas blíže k sobě.
- **Proměnná Zdroj** – Zahrnuje sadu použitelných zdrojů a dá se omezit vyřazením zdrojů ze seznamu.

#### <a name="constraint"></a>Omezení

Omezení funguje tak, že omezí sady u proměnných, ale také závisí na jiných proměnných, takže se aktivuje při změně proměnných. Proces „šíření omezení“ představuje vykonání hlavní funkce omezení, a je-li úspěšný, provede zpětné hlášení do hlavní logiky.

Proměnná se považuje za vázanou, když ji nelze dále omezovat, což pro proměnnou DateTime znamená, že horní a dolní mez je stejná, a pro proměnnou Resource, že má jen jeden použitelný zdroj. Když jsou všechny proměnné vázané, najde se řešení.

### <a name="constraint-levels"></a>Úrovně omezení

Když je plánování prováděno jako součást fáze pokrytí plánování požadavků na materiál (MRP), budou zakázky naplánovány zpětně od data požadavku. Pokud však není možné najít plán, který začíná dnes nebo později a končí před požadovaným datem, změní se směr plánování na ode dneška.

Toto hlavní obchodní pravidlo se řeší uspořádáním omezení v úrovních. V případě, že se při použití omezení na nejvyšší úrovni nenajde žádné řešení, všechna omezení na této úrovni se zruší a vyzkouší se nižší úroveň. V praxi to znamená, že pro zpětné plánování bude model obsahovat úroveň 1 s cíli úloh, které odpovídají nejpozdějšímu času zahájení, aby se vyhovělo maximálnímu omezení koncového času (požadovanému datu), a úroveň 0 s cíli úloh, které odpovídají nejčasnějšímu koncovému času s tím, že platí omezení minimálního počátečního času, a to na dnešek.

### <a name="algorithm"></a>Algoritmus

Hlavní kroky algoritmu modulu:

1. Najde posloupnosti (řetězce úloh), které lze vyřešit samostatně.
1. Pokusí se najít počáteční řešení pro sekvenci s nejvyšší úrovní omezení.
    1. Seřadí úlohy v posloupnosti podle cíle a priorit úloh, aby bylo možné najít počáteční úlohu.
    1. Vytvoří cyklus úloh v následující posloupnosti:
        1. Najde všechna omezení, která je třeba rozšířit, a spustí šíření.
        1. Pokud byly všechny proměnné pro úlohu svázány, našlo se řešení pro tuto úlohu.
        1. Pokud jednu z proměnných nelze svázat bez porušení omezení, pak vrátí zpět vazbu proměnné, zkusí jinou hodnotu v sadě (pro proměnnou zdroje) a znovu zahájí šíření omezení.
1. Pokud nebylo nalezeno žádné řešení, budou odstraněna všechna omezení na aktuální úrovni omezení, úroveň omezení se sníží (pokud jsou k dispozici nižší úrovně) a hledání řešení se zopakuje s novou sadou omezení.
1. Pokud bylo nalezeno proveditelné řešení, je zahájena fáze optimalizace, což je snaha hledat lepší řešení, dokud nebude dosažen časový limit optimalizace nebo dokud nebudou vyčerpány všechny kombinace zdrojů.

Řešitel omezení nemá povědomí o specificích plánovacího algoritmu. Celé „kouzlo“ spočívá v definici a kombinaci různých omezení.

### <a name="determining-working-times"></a>Určení pracovních časů

Velká část (interních) omezení v modulu řídí pracovní dobu a kapacitu zdroje. Úloha v podstatě spočívá v procházení slotů pracovní doby pro zdroj z daného bodu v daném směru a nalezení dostatečně dlouhého intervalu, do kterého se vejde požadovaná kapacita (čas) úloh.

K tomu modul potřebuje znát pracovní dobu zdroje. Oproti hlavním datům modelu se pracovní doby *načítají v líném režimu*, což znamená, že se do modulu načítají podle potřeby. Důvodem pro tento přístup je, že v Supply Chain Managementu často existují pracovní doby pro kalendář na velmi dlouhé období a obvykle existuje mnoho kalendářů, takže data by byla pro předběžné načtení poměrně velká.

Informace z kalendáře si modul žádá v blocích vyvoláním metody třídy X++ `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Požadavek je pak na konkrétní ID kalendáře v konkrétním časovém intervalu. V závislosti na stavu mezipaměti serveru v Supply Chain Managementu může každý z těchto požadavků vést k několika voláním databáze, což trvá dlouho (relativně k čistému výpočetnímu času). Pokud navíc kalendář obsahuje velmi propracované definice pracovní doby s mnoha intervaly za den, prodlouží se čas, který načítání zabere.

Když se do plánovacího modulu načtou data o pracovní době, tato se udrží v interní mezipaměti pro konkrétní kalendář, což znamená, že pokud jakékoli jiné úlohy nebo zdroje používají stejný kalendář, lze další vyhledávání rychle provést z této paměti. Jednou z běžných příčin špatného výkonu je, že je pro každý zdroj použito samostatné ID kalendáře, protože pro každý kalendář bude poté nutné požadovat data, přestože obsah kalendářů může být stejný.

### <a name="finite-capacity"></a>Omezená kapacita

Při použití omezené kapacity se pracovní časové intervaly z kalendáře rozdělí a sníží na základě stávajících rezervací kapacity. Tyto rezervace se také načítají prostřednictvím stejné třídy `WrkCtrSchedulingInteropDataProvider` jako kalendáře, ale tentokrát se používá metoda `getCapacityReservations`. Během hlavního plánování se berou v úvahu rezervace konkrétního hlavního plánu, a pokud jsou povoleny na stránce **Parametry hlavního plánování**, zahrnou se i rezervace z potvrzených výrobních zakázek. Podobně také při plánování výrobní zakázky existuje možnost zahrnout rezervace ze stávajících plánovaných objednávek, i když to není tak běžné jako naopak.

Použití omezené kapacity způsobí, že plánování bude trvat déle, a to z několika důvodů:

- Načítání informací o kapacitě z databáze je pomalá operace a ukládání informací o kapacitě do mezipaměti na straně serveru obvykle není tak efektivní jako u pracovních časů, protože se nesdílí mezi zdroji, což obvykle platí pro kalendáře.
- Počet slotů pracovní doby, které se mají procházet, se zvyšuje kvůli jejich rozdělení a obvykle musí být prozkoumány sloty pro delší časové období, než bude možné najít řešení.
- Po dokončení plánování je třeba provést kontrolu konfliktních rezervací (podrobnosti viz část Paralelní spuštění více plánovacích modulů).

### <a name="examining-the-resource-combinations"></a>Zkoumání kombinací zdrojů

Pokud sekvence úloh obsahuje pouze standardní propojení `FinishStart`, což znamená, že tvoří jednoduchý řetězec bez větví, lze optimálního výsledku (z pohledu jedné zakázky, nikoli napříč zakázkami) dosáhnout nalezením nejlepšího řešení pro první úlohu a následným přechodem k nalezení nejlepšího řešení pro další úlohu. Nejlepším řešením úlohy je nalezení zdroje, který se dokáže co nejblíže dostat k cílovému počátečnímu a koncovému datu úlohy (při dopředném plánování to znamená zajištění co nejdřívějšího koncového data úlohy), při současném respektování omezení.

Pokud existují paralelní úlohy, hledání řešení může s sebou nést zkoumání různých kombinací zdrojů. Počet možných kombinací zdrojů je součinem počtu použitelných zdrojů pro připojené paralelní úlohy. Zejména při zpětném plánování zakázky od požadovaného data může logice chvíli trvat, než zjistí, že neexistuje žádné řešení problému, aby paralelní úlohy nespadaly před dnešní datum, protože bude nutné zkontrolovat všechny kombinace vzhledem k tomu, že by mohly existovat nějaké zdroje, které by měly vyšší účinnost, nebo jiný kalendář, který by mohl přinést výsledek. To znamená, že pokud nebyl nastaven žádný časový limit, poběží dlouho, než změní směr na vpřed.

Tato kombinatorická logika také znamená, že přidání více použitelných zdrojů může způsobit pomalejší chod modulu. Pokud dojde k problémům s výkonem při paralelních operacích a plánování s neomezenou kapacitou, lze to částečně vyřešit tak, že návrhář trasy přijme rozhodnutí o tom, který prostředek by měl být použit, a poté prostředek přiřadit přímo k operaci (protože modul ve většině případů vždy nakonec vybere stejný zdroj, takže konečný výsledek bude stejný).

### <a name="hard-links"></a>Pevná propojení

Nastavením pevného typu propojení mezi dvěma úlohami zajistíte, že mezi dokončením jedné úlohy a začátkem další nebude žádná časová prodleva. To může být velmi užitečné v určitých scénářích, třeba když se v jedné úloze zahřívá kov a poté se zpracovává v další úloze, přičemž není žádoucí nechat kov mezi úlohami vychladnout.

Se standardními měkkými propojeními a plánováním dopředu platí, že pokud trasa tvoří jednoduchý řetězec bez větví, lze dosáhnout výsledku nalezením řešení pro první úlohu, které splňuje svá vlastní omezení, a poté pokračováním v řetězci šířením času dokončení z předchozí úlohy na další. Pokud aktuální úloha nemůže najít žádnou kapacitu, počáteční čas pro ni se posune dále, bez následků pro předchozí úlohy, čímž by potenciálně mohly vznikat prodlevy mezi úlohami. Avšak u pevných propojení (zejména ve spojení s omezenou kapacitou) pro stejný scénář bude skutečnost, že jedna úloha později v řetězci nemůže najít kapacitu, znamenat, že všechny předchozí naplánované úlohy budou muset být jedna po druhé „přetaženy“, a tím několikrát přeplánovány. Zejména ve scénářích s vysokým zatížením více zdrojů můžou pevná propojení způsobit řetězovou reakci, při které se úlohy budou navzájem ovlivňovat a bude se muset provést řada iterací, než se výsledek stabilizuje do proveditelného plánu.

## <a name="running-scheduling-engines-in-parallel"></a>Paralelní spuštění plánovacích modulů

Když provádíte plánování jako součást běhu hlavního plánování, kde se používají podpůrná vlákna, může úlohy plánování výrobní zakázky vybírat také každé z těchto vláken. To znamená, že může běžet více plánovacích modulů současně. I když je multithreading obecně velmi významná výhoda v oblasti výkonu, existují také některé funkční nevýhody v oblasti plánování.

V MRP jsou všechny výrobní zakázky pro danou úroveň kusovníku (BOM) naplánovány v sekvenci požadovaných dat, což znamená, že zakázky s nejdřívějším požadovaným datem by měly být naplánovány jako první, takže mají nejvyšší šanci na získání dostupné kapacity zdrojů. Když si ale více modulů vybírá ze seznamu nenaplánovaných zakázek, posloupnost už není zajištěna, protože jedna může být dokončena rychleji než jiné.

Při plánování při omezené kapacitě a při pokusu více instancí modulu naplánovat zakázky, které potenciálně používají stejné zdroje ve stejném časovém intervalu, může navíc dojít ke konkurenčním požadavkům. Počet takových konkurenčních požadavků je zaznamenán v poli **Plánování konfliktů** na stránce historie hlavních plánů. Logika řešení těchto konfliktů:

- Naplánuje se zakázka (bez zámku) a získají se rezervace kapacity.
- Nastaví se zámek.
- Zkontroluje se, zda u naplánovaných zdrojů v časovém rozsahu existují novější rezervace kapacity.
  - Pokud ne, kapacita se zapíše a uvolní se zámek.
  - Pokud ano, uvolní se zámek a zakázka se naplánuje od začátku.

Takže při plánování s více instancemi modulu není výsledek plně deterministický, protože bude záviset na přesném načasování každého z vláken.

## <a name="operation-scheduling-performance"></a>Výkon při plánování operací

I když se plánování operací označuje také jako hrubé plánování kapacity, z pohledu modulu to může být těžší problém k vyřešení, pokud se používá omezená kapacita, protože k určení proveditelnosti je zapotřebí více dat.

Kapacita skupiny zdrojů závisí na tom, které zdroje a kolik je členy této skupiny. Skupina zdrojů sama o sobě nemá žádnou kapacitu – pouze v případě, že jsou členem skupiny zdroje, bude mít jejich kapacitu. Vzhledem k tomu, že se členství ve skupině zdrojů může časem měnit, je nutné kapacitu denně vyhodnocovat.

V plánování operací se kalendář skupiny zdrojů používá k určení časů zahájení a ukončení každé operace. To znamená, že kalendář skupiny zdrojů omezuje, kolik času můžou být operace naplánované na jednu operaci v jeden den v jedné skupině zdrojů. Oproti kalendáři pro konkrétní zdroje jsou údaje z kalendáře skupiny zdrojů ignorovány kvůli své neefektivitě, protože – zjednodušeně řečeno – označují otevírací dobu a nikoli skutečnou kapacitu.

Pokud je například pracovní doba skupiny zdrojů v konkrétní den od 8:00 do 16:00, jedna operace nemůže u této skupiny vytvořit větší zatížení než to, co lze zvládnout za 8 hodin, a to bez ohledu na to, jak velkou kapacitu má daná skupina k dispozici celkem v daný den. Zatížení však může dále omezit skutečná dostupná kapacita.

Při výpočtu dostupné kapacity pro skupinu zdrojů v daný den se zohlední zatížení z naplánovaných úloh u všech zdrojů zahrnutých do této skupiny v tentýž den. Pro každé datum probíhá výpočet takto:

*Dostupná kapacita skupiny prostředků = kapacita zdrojů ve skupině na základě jejich kalendáře &ndash; Naplánované zatížení z úloh u zdrojů ve skupině &ndash; Naplánované zatížení z operací u zdrojů ve skupině &ndash; Naplánované zatížení z operací ve skupině zdrojů*

Na kartě **Požadavky na zdroj** u operace postupu lze požadavky na zdroj zadat buď jako konkrétní zdroj (v takovém případě bude operace naplánována s použitím tohoto zdroje), jako skupinu zdrojů, jako typ zdroje, nebo jako jednu či více schopností (dovednost, kurz či certifikát). Použití všech těchto možností poskytuje velkou flexibilitu při návrhu trasy, zároveň však komplikuje plánování na modulu, protože u kapacity musí být zohledněna každá „vlastnost“ (abstraktní název používaný v modulu pro schopnosti, dovednosti atd.).

Kapacita skupiny zdrojů, pokud jde o určitou schopnost, je součet kapacity ze všech zdrojů ve skupině, která tuto schopnost mají. Pokud má zdroj ve skupině určitou schopnost, bude to zohledněno bez ohledu na požadovanou úroveň kapacity.

V plánování operací se dostupná kapacita pro určitou schopnost ve skupinu zdrojů sníží, když je zatížená operací, která dotyčnou schopnost vyžaduje. Pokud operace vyžaduje více než jednu schopnost, kapacita se sníží pro všechny požadované funkce.

Pro každé datum probíhá požadovaný výpočet takto:

*Dostupná kapacita pro schopnost = Kapacita pro schopnost &ndash; Naplánované zatížení z úloh u zdrojů, které tuto konkrétní schopnost mají, ve skupině zdrojů &ndash; Naplánované zatížení z operací u zdrojů, které tuto konkrétní schopnost mají, ve skupině zdrojů &ndash; Naplánované zatížení z operací, které tuto schopnost vyžadují, u samotné skupiny zdrojů*

To znamená, že pokud existuje zatížení konkrétního zdroje, zohlední se při výpočtu dostupné kapacity skupiny zdrojů, pokud jde o konkrétní schopnost, protože zatížení konkrétního zdroje snižuje jeho příspěvek k její kapacitě, pokud jde o danou schopnost, a to bez ohledu na to, zda toto zatížení s touto konkrétní schopností souvisí. Pokud existuje zatížení na úrovni skupiny zdrojů, zohlední se to při výpočtu její dostupné kapacity, pokud jde o konkrétní schopnost, jen v případě, že zatížení pochází z operace, která tuto konkrétní schopnost vyžaduje.

Výše uvedená logika je komplikovaná, protože je stejná pro každý typ „vlastnosti“, takže použití plánování operací s omezenou kapacitou vyžaduje načtení významného objemu dat.

## <a name="viewing-scheduling-engine-input-and-output"></a>Zobrazení vstupu a výstupu plánovacího modulu

Chcete-li získat konkrétní podrobnosti o vstupu a výstupu procesu plánování, povolte protokolování přechodem na **Správa organizace \> Nastavení \> Plánování \> Kokpit pro trasování plánování**.

Na této stránce nejprve vyberte **Povolit protokolování** v podokně akcí. Pak určete plánování výrobní zakázky. Po dokončení se vraťte na stránku **Kokpit pro trasování plánování** a vyberte **Zakázat protokolování** v podokně akcí. Obnovte stránku a v mřížce se objeví nový řádek. Vyberte nový řádek a pak **Stáhnout** v podokně akcí. Získáte tím komprimovanou složku ZIP obsahující následující soubory:

- **Log.txt** – Toto je soubor protokolu, který popisuje kroky, kterými modul prochází. Je to velmi detailní a může se zdát, že je toho příliš, ale při použití v rámci experimentování s nastavením trasy s cílem vyřešit problémy s výkonem je třeba se nejprve podívat na časový rozdíl mezi prvním a posledním řádkem, protože tím zjistíte přesný čas, který plánovač potřeboval.
- **XmlModel.xml** – Obsahuje model sestavený v X++, na němž modul pracuje. Položka `JobId` použitá v souboru koreluje s položkou `RecId` ze zdrojové tabulky obsahující úlohy (`ReqRouteJob` nebo `ProdRouteJob`). Typickou věcí, kterou je třeba v tomto souboru zkontrolovat, je, že data uvedená v položkách `ConstraintJobStartsAt` a `ConstraintJobEndsAt` jsou podle očekávání, že vlastnost `JobGoal` je nastavena správně a že úlohy spolu souvisejí prostřednictvím omezení `JobLink`.
- **XmlSlots.xml** – Obsahuje všechny pracovní doby a rezervace kapacity, které modul požadoval. Pracovní doby a rezervace v kalendáři budou modulem vyžadovány pouze pro časová období, do nichž se pokouší úlohy (a další vyrovnávací paměť) umístit, takže pokud soubor obsahuje časy velmi daleko v budoucnosti, může to být indikací problému s nastavením. Uzly `ResourceProperty` zobrazí u každého zdroje, se kterou skupinou prostředků a schopnostmi je spojen v konkrétních obdobích.
- **Result.xml** – Obsahuje výsledek běhu plánování.

Všimněte si, že funkce trasování může z hlediska výkonu významně zvýšit režii, proto ji používejte pouze k prozkoumání plánování konkrétních zakázek kontrolovaným způsobem. Pokud je zapnutá během hlavního plánování, rychle dosáhne svého limitu velikosti a zastaví se.

## <a name="troubleshooting-performance"></a>Řešení problémů s výkonem

Jak lze pochopit ze všech předchozích částí, existují určité úskalí, pokud jde o nastavení a použití plánovacího modulu, což může vést k problémům s výkonem. Lze je vyřešit pomocí následujícího kontrolního seznamu. Je důležité podívat se na všechny body, protože problémy nejčastěji způsobuje kombinace více faktorů.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Provádění plánování v rámci MRP, když to není potřeba

I když se trasy používají pro účely řízení výroby, jako je kalkulace nákladů a vykazování, nemusí být nutné je během MRP brát v úvahu. V některých případech bude pro plánování stačit standardní doba realizace výroby stanovená pro položku. Chcete-li vypnout plánování trasy, nastavte časové ohraničení kapacity na nulu. Pokud by mělo být provedeno plánování, musí být časové ohraničení kapacity nastaveno pečlivě, protože nemusí být nutné brát v úvahu trasy v celém rozsahu časového ohraničení pokrytí MRP.

Všimněte si, že pokud zakázka není naplánována během MRP, bude třeba ji naplánovat, až bude plánovaná zakázka potvrzena. To znamená, že proces potvrzení bude trvat déle, takže v závislosti na tom, u kolika z navržených plánovaných objednávek dojde k potvrzení, může ve fázi MRP dojít ke ztrátě výkonu při potvrzování.

### <a name="route-with-unnecessary-operations"></a>Trasa se zbytečnými operacemi

Při navrhování trasy je lákavé pokusit se přesně namodelovat skutečný průběh se všemi kroky, kterými výroba prochází. I když to může být v některých případech užitečné, není to dobré pro výkon, protože model, s nímž musí modul pracovat, se zvětší (z hlediska úloh i omezení) a bude provedeno více příkazů SQL pro vkládání a aktualizaci úloh a rezervace kapacity. Existuje také následný efekt spočívající v tom, že je třeba hlásit pokrok u úloh, což lze zmírnit automatickým účtováním. Pokud se tato data k ničemu nepoužívají, vytváří zbytečné zatížení.

Doporučujeme, abyste vytvořili pouze operace, které je vyloženě třeba naplánovat (což jsou obvykle ty, které představují úzké hrdlo) nebo pro účely výpočtu nákladů. Alternativou je seskupení mnoha menších různorodých operací do jedné větší operace, která bude představovat větší část procesu.

### <a name="many-applicable-resources-for-an-operation"></a>Mnoho použitelných zdrojů pro operaci

Počet použitelných zdrojů pro operaci je určen požadavky na zdroje nastavenými ve vztahu operace. Požadavek může být buď na konkrétní (jednotlivý) zdroj, případně může být založen na členství zdroje ve skupině zdrojů nebo na jeho schopnosti.

Pokud se plánování neprovádí s použitím omezené kapacity a všechny použitelné zdroje mají stejný kalendář a účinnost, pak plánovací modul vždy vybere pro operaci stejný zdroj, ale až po vyzkoušení všech použitelných zdrojů, aby zkontroloval, zda není k dispozici nějaký „lepší“. V tomto případě lze značně snížit zatížení plánování jednoduše tím, že v době návrhu trasy operaci vždy přiřadíte konkrétní zdroj.

### <a name="route-with-parallel-operations"></a>Trasa s paralelními operacemi

Paralelní operace (primární/sekundární) jsou sice výkonným nástrojem pro modelování scénářů, třeba kdy je k provedení konkrétního úkolu potřeba stroj i operátor, ale současně jsou zdrojem mnoha problémů s výkonem. Pokud je požadavek na konkrétní jednotlivý zdroj přiřazen k primární i sekundární operaci, obvykle to není problém. Pokud ale existuje mnoho možných zdrojů pro každou z operací, vnese to do plánování významnou výpočetní složitost.

Alternativou k použití paralelních operací je buď modelování těchto párů jako „virtuálních“ zdrojů (které pak budou reprezentovat „týmy“, které jdou do operace vždy společně), nebo se jednoduše při modelování jedna z operací vynechá, pokud nepředstavuje úzké hrdlo.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Trasa s počtem zdrojů vyšším než 1

Pokud množství zdrojů potřebných pro operaci nastavíte na hodnotu vyšší než 1, pak to bude mít v podstatě stejný výsledek jako použití primárních/sekundárních operací, protože do modulu se bude odesílat více paralelních úloh. V tomto případě však neexistuje možnost přiřazení konkrétních prostředků, protože množství vyšší než 1 vyžaduje, aby byl pro operaci použitelný více než 1 zdroj.

### <a name="excessive-use-of-finite-capacity"></a>Nadměrné používání omezené kapacity

Použití omezené kapacity vyžaduje, aby modul načetl informace o kapacitě z databáze, a může mít výpočetní režii, protože bude obtížnější najít řešení, zejména v prostředích, kde jsou prostředky rezervovány blízko své maximální kapacity. V důsledku toho je důležité pečlivě vyhodnotit, zda zdroj skutečně potřebuje využívat omezenou kapacitu, nebo zda je možné ho rezervovat nadměrně. Protože mezi prostředky s omezenou kapacitou může existovat rozdíl v tom, jak důležité je, aby u nich nedošlo k nadměrné rezervaci, doporučujeme u zdroje použít možnost úzkého hrdla v kombinaci se samostatnou hodnotou v plánu v části Ochranná doba kapacity pro kritické prostředky. Koncept úzkého hrdla umožňuje snížení obecného časového ohraničení konečné kapacity.

### <a name="setting-hard-links"></a>Nastavení pevných propojení

Standardní typ propojení u trasy je *měkký*, což znamená, že mezi dobou ukončení jedné operace a začátkem další je povolena časová prodleva. Pokud to povolíte, může to mít ten neblahý účinek, že pokud pro některou z operací nebudou materiály nebo kapacita k dispozici po velmi dlouhou dobu, může být výroba nějakou dobu nečinná, čímž může narůst množství rozpracované práce. U pevných propojení se to nestane, protože dokončení a zahájení musí dokonale navazovat. Nastavení pevných odkazů ale problém s plánováním ztěžuje, protože průsečíky pracovní doby a kapacity je nutné vypočítat pro dva zdroje operací. Pokud jsou součástí i paralelní operace, výrazně tím vzroste výpočetní čas. Pokud zdroje u těchto dvou operací mají různé kalendáře, které se vůbec nepřekrývají, problém je neřešitelný.

Pevná propojení doporučujeme používat, pouze pokud je to nezbytně nutné, a pečlivě zvažte, zda je to nezbytné pro každou operaci trasy.

Trikem, jak omezit množství rozpracované práce bez použití pevných propojení, je naplánovat zakázku dvakrát, přičemž u druhého průchodu se směr změní na opačný. Pokud by se první plán nastavil zpětně od data dodání, druhý by se měl být provádět dopředu od naplánovaného data zahájení. To způsobí, že úlohy budou co nejvíce komprimovány, takže objem rozpracované práce bude minimalizován.

### <a name="separate-calendar-for-each-resource"></a>Samostatný kalendář u každého zdroje

Jedním z hlavních zdrojů dat pro plánovací modul jsou informace z kalendáře, jejichž načítání z databáze může být nákladné. Protože kalendáře jsou generovány na základě šablon, může být lákavé vygenerovat kalendář pro každý zdroj a poté upravit informace v tomto kalendáři, když u zdroje dojde k výpadku a dalším problémům. Tímto způsobem však vážně omezíte schopnost modulu ukládat data z kalendáře do mezipaměti, protože by bylo nutné požadovat nová data pro každý zdroj, což by mohlo být velkým zdrojem problémů s výkonem. Místo toho doporučujeme, abyste mezi zdroji co nejvíce používali stejné kalendáře a poté změny vyplývající z prostojů implementovali přiřazením jiného ID kalendáře pro konkrétní období.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Vysoký počet slotů pracovní doby pro kalendářní den

Protože modul pracuje tak, že prozkoumává jednotlivé časové sloty z hlediska kapacity, je výhodné minimalizovat počet časových slotů v kalendářním dni. Toho lze dosáhnout například tím, že zvážíte, zda je důležité, aby výsledný plán odrážel, že pracovníci mají každou hodinu 5minutovou přestávku.

### <a name="large-or-none-scheduling-timeouts"></a>Velké (nebo žádné) časové limity plánování

Výkon plánovacího modulu lze optimalizovat pomocí parametrů na stránce **Parametry plánování**. Nastavení **Časový limit plánování povolen** a **Časový limit optimalizace plánování povolen** by mělo být vždy nastaveno na **Ano**. Pokud je nastaveno na **Ne**, plánování může potenciálně běžet nekonečně dlouho, pokud byla vytvořena neproveditelná trasa s mnoha možnostmi.

Hodnota **Maximální čas plánování na sekvenci** určuje, kolik sekund lze nanejvýš strávit pokusem najít řešení pro jednu sekvenci (ve většině případů sekvence odpovídá jedné zakázce). Hodnota, která se zde použije, velmi závisí na složitosti trasy a nastaveních, jako je konečná kapacita – dobrým výchozím bodem je maximálně asi 30 sekund.

Hodnota **Časový limit pokusů o optimalizaci** určuje, kolik sekund lze maximálně využít k nalezení lepšího řešení, než jaké bylo původně nalezeno. To ovlivní pouze trasy, které používají paralelní operace, protože kvůli nim je nutné otestovat různé kombinace.

> [!NOTE]
> Hodnoty nastavené pro časové limity budou použity jak pro plánování vydaných výrobních zakázek, tak plánovaných zakázek v rámci MRP. Výsledkem je, že nastavení velmi vysokých hodnot by mohlo výrazně zvýšit dobu běhu MRP při spuštění plánu s mnoha naplánovanými výrobními zakázkami.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]