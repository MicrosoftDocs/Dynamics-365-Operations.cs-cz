---
title: Přehled struktur rozpisu prací
description: Strukturovaný rozpis prací (WBS) je popis práce, která bude provedena v projektu. Jedná se o hierarchii úkolů, která představuje pochopení projektového týmu v souvislosti se složením práce a velikostí, náklady a dobou trvání jednotlivých součástí nebo úkolů.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78509898d0c2279750df3860a670d3d7a6badfc0
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865573"
---
# <a name="work-breakdown-structures-overview"></a>Přehled struktur rozpisu prací

[!include [banner](../includes/banner.md)]

Strukturovaný rozpis prací (WBS) je popis práce, která bude provedena v projektu. Jedná se o hierarchii úkolů, která představuje pochopení projektového týmu v souvislosti se složením práce a velikostí, náklady a dobou trvání jednotlivých součástí nebo úkolů. WBS má tři hlavní účely:

-   Popis rozpisu nebo složení prací v úkolu.
-   Plánování práce na projektu.
-   Odhad nákladů na jednotlivé úkoly.

Úroveň podrobností ve WBS závisí na přesnosti, která je nutná v odhadech, a úrovni sledování, které je nutné pro tyto odhady. Projekty, které mají velmi nízkou toleranci pro zaostávání za plánem nebo náklady, obvykle vyžadují podrobnější WBS a důkladné sledování průběhu práce a nákladů vzhledem k WBS. Tento typ projektu je běžný ve stavebnictví a strojírenství. 

Naproti tomu projekty v jiných odvětvích, jako jsou například média a inzerce, software a IT infrastruktura, jsou obvykle jedinečné a produktivita je závislá na zkušenostech a kompetencích osoby, která provádí úkoly. Tyto odvětví tedy využívají WBS k určení přibližné velikosti projektu, nikoli k podrobnému sledování průběhu tohoto projektu. 

Vytvoření WBS je náročný proces, který obvykle probíhá dlouhou dobu a vyžaduje spolupráci a informace od různých osob. Toto téma popisuje použití vylepšení struktury WBS v aplikaci Microsoft Dynamics 365 for Finance and Operations, aby byly splněny požadavky pro odhady a sledování.

## <a name="prerequisites-for-creating-a-wbs"></a>Předpoklady pro vytvoření WBS
Chcete-li vytvořit strukturu WBS, je nutné vytvořit pracovní rozvrh a odhad nákladů prací.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Předpoklady pro vytvoření pracovního rozvrhu

Chcete-li použít funkce úplného plánování struktury WBS, proveďte následující nastavení:

1.  Nastavení výchozího kalendáře a kalendáře projektu:
    1.  Klikněte na **Řízení a účetnictví projektů** &gt; **Nastavení** &gt; **Parametry modulu Řízení a účetnictví projektu.** &gt; **Plánování**. V poli **Výchozí pracovní kalendář** upřesněte výchozí kalendář. Ten se stane výchozím pracovním kalendářem pro všechny nové vytvořené projekty.
    2.  Výchozí kalendář pro konkrétní projekt můžete změnit. Klikněte na stránku s podrobnostmi o projektu a poté na pevné záložce **Projektový tým a plánování** aktualizujte pole **Plánovací kalendář** výběrem jiného kalendáře.

2.  Nastavte standardní pracovní dny a pracovní dobu. Kalendář, který nastavíte jako pracovní kalendář projektu, se použije ve WBS k určení následujících informací:

-   Pracovní dny a svátky
-   Počet pracovních hodin za den

Chcete-li nastavit pracovní dny a pracovní dobu pro kalendář nebo vytvořit nový kalendář, klikněte na položky **Správa organizace** &gt; **Obecně** &gt; **Kalendáře**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Předpoklady pro odhad nákladů na práci

Chcete-li použít úplné funkce odhadu nákladů ve struktuře WBS, měli byste nastavit náklady a prodejní ceny pro zaměstnance, kategorie práce, výdaje, poplatky a položky.

-   Chcete-li nastavit náklady a prodejní cenu práce, výdajů a kategorií poplatků, klikněte na položky **Řízení a účetnictví projektů** &gt; **Nastavení** &gt; **Ceny**.
-   Chcete-li nastavit náklady a prodejní ceny zboží, použijte stránku **Obchodní smlouvy** pro každou položku na stránce seznamu **Uvolněné produkty** v modulu řízení informací o produktu.

## <a name="creating-a-wbs"></a>Vytváření WBS
Vytvoření struktury WBS zahrnuje tři aktivity:

1.  **Dekompozice práce** – Vytvořte rozpis práce na spravovatelné bloky nebo úkoly.
2.  **Pracovní rozvrh** – Odhadněte čas potřebný k dokončení úkolu, nastavte vzájemné závislosti úkolů a vyberte počáteční a koncové datum pro úkoly.
3.  **Odhad nákladů** – Odhad nákladů pro každý úkol.

Následující části popisují, jak vám možnosti struktury WBS mohou pomoci v každé z těchto aktivit.

### <a name="work-decomposition"></a>Dekompozice práce

Vytvoření rozpisu nebo dekompozice práce je obvykle prvním krokem při vytváření struktury WBS. Funkce struktury WBS podporuje následující základní konstrukce rozpisu nebo dekompozice práce. 

**Kořenový úkol projektu** Kořenový úkol projektu je úkol na nejvyšší úrovni souhrnu pro projekt. Pod ním jsou vytvořeny všechny ostatní úkoly projektu. Název kořenového úkolu je vždy nastaven na název projektu. Úsilí, data a období platnosti kořenového uzlu sumarizuje hodnoty úkolů pod kořenovým úkolem. Nelze upravit vlastnosti kořenového uzlu ani je odstranit.

**Úkoly souhrnu nebo kontejneru** Souhrnný úkol je úkol, který má pod sebou dílčí úkoly nebo jednotlivé úkoly. Souhrnný úkol nemá žádné vlastní pracovní úsilí ani náklady. Místo toho pracovní úsilí a nákladů na souhrnný úkol jsou součtem pracovního úsilí a nákladů na jednotlivé úkoly. Nejbližší datum zahájení jednotlivých úkolů se používá jako počáteční datum souhrnného úkolu a nejpozdější koncové datum jednotlivých úkolů se používá jako koncové datum. Můžete upravit název souhrnného úkolu, ale nelze změnit vlastnosti plánování – úsilí, data a dobu trvání. Při odstranění souhrnného úkolu odstraníte také všechny jednotlivé úkoly. 

**Úkoly listového uzlu** Úkol listového uzlu představuje nejvíce podrobný balíček práce na projektu. Listový uzel má odhadované úsilí, plánovaný počet prostředků, plánované počáteční a koncové datum a dobu trvání. 

Můžete provést následující operace hierarchie, chcete-li povolit vytvoření pracovní hierarchie nebo dekompozice pro projekt. 

**Nový úkol** Jakýkoli nový úkol, který vytvoříte, se automaticky přidá pod kořenový uzel, a číslo WBS je automaticky přiřazeno k úkolu. Číslo WBS představuje úroveň úkolu v hierarchii. Pro úkoly na první úrovni pod kořenovým úkolem projektu se používá schéma číslování 1, 2, 3 a tak dále. Pro úkoly pod první úrovni se používá schéma číslování 1.1, 1.2, 1.3 a tak dále. Pro každou úroveň přidanou pod předchozí úroveň je přidána nová tečkovaná řada čísel. 

V současné době nelze měnit číslování struktury WBS. 

**Odsazení úkolu** Když odsadíte úkol, stane podřízeným předcházejícího úkolu. Číslo WBS nového podřízeného úkolu je automaticky přepočítáno na základě čísla WBS nového nadřazeného úkolu. Nadřazený úkol je nyní úkolem souhrnu nebo kontejneru, a proto bude shrnutím jednotlivých úkolů. 

> [!NOTE] 
> Po odsazení úkolů pod úkolem, který byl listovým uzlem před operací odsazení, nově vytvořené souhrnné úkoly ztratí vlastní data, úsilí a počet prostředků. Nyní používá souhrn hodnot nových jednotlivých úkolů. 

**Předsazení úkolu** Při předsazení úkolu již není jednotlivým úkolem nadřazeného úkolu. Číslo struktury WBS tohoto úkolu bude automaticky přepočítáno tak, aby odráželo novou úroveň úkolu v hierarchii. Úsilí, náklady a data předchozího nadřazeného úkolu jsou přepočítány, aby byl tento úkol vyloučen. 

**Přesunout nahoru a Přesunout dolů** Kliknutím na tlačítko **Přesunout nahoru** a **Přesunout dolů** změníte pozici úkolu v rámci hierarchie nadřazené sady. Pozice úkolu neovlivní úsilí, náklady, data nebo dobu trvání úkolu. Číslo struktury WBS úkolu však bude automaticky přepočítáno tak, aby odráželo novou pozici úkolu.

### <a name="schedule-estimation"></a>Odhad plánu

Odhad plánu je obvykle druhým krokem při vytváření struktury WBS. Doporučujeme provést odhad plánu po vytvoření úkolů. Stránka **Strukturovaný rozpis prací** v aplikaci Finance and Operations má dvě části. Horní podokno je určeno pro odhad plánu a dolní podokno obsahuje kartu **Odhadované náklady a výnosy**, kterou lze použít pro odhady nákladů. 
**Závislosti úkolu** Ve WBS můžete vytvořit vztahy předchůdců mezi úkoly. Když přiřadíte předcházející úkoly k úkolu, lze tento úkol zahájit až po dokončení všech jeho předchůdců. Plánované datum zahájení úkolu je automaticky nastaveno na poslední datum všech jeho předchůdců. 

**Plánování úkolů v aplikaci Microsoft Dynamics 365 for Finance and Operations** Následující faktory určují plánování úkolů listového uzlu:

-   Předchůdci
-   Úsilí
-   Počet prostředků
-   počáteční a konečné datum.

Počáteční datum úkolu listového uzlu, který nemá předchůdce, bude automaticky nastaveno na počáteční datum plánování projektu. Trvání úkolu listového uzlu se vždy počítá jako počet dní mezi jejich počátečním a koncovým datem. 

*<strong><em>Pravidla plánování</em></strong>* Je-li zapnuta pomoc s automatickým plánováním, platí na plánování úkolů pro úkoly listového uzlu následující pravidla:

-   Počáteční a koncové datum úkolu musí být v pracovní dny, podle kalendáře pro plánování projektu.
-   Počáteční datum úkolu, který má předchůdce, je automaticky nastaveno na poslední koncové datum všech jeho předchůdců.
-   Úsilí úkolu se automaticky vypočítá následujícím způsobem:

Počet lidí x doba trvání x počet hodin ve standardním pracovním dni v projektovém kalendáři. 

V některých případech se můžete chtít odchýlit od těchto pravidel. Můžete vypnout automatické plánování, chcete-li aplikaci Finance and Operations zabránit v automatickém nastavení nebo opravě všech vlastností úkolů listových uzlů. Při zadání informací o úkolu, který způsobí porušení pravidel plánování, se pro úkol zobrazí ikona chyby plánování. Pokud nechcete, aby se chyby plánování zobrazovaly, kliknutím na možnost **Chyby plánování jsou zobrazeny** tuto funkci zakážete. 

> [!NOTE] 
> Hodnoty pro úkoly souhrnu nebo kontejneru budou i nadále počítány jako součet hodnot jednotlivých úkolů, bez ohledu na to, zda je pomoc s automatickým plánováním zapnuta nebo vypnuta. 

**Oprava chyb plánování** Je-li pomoc s automatickým plánováním zapnuta, pravděpodobně nedojde k chybám plánování. Je-li pomoc s automatickým plánováním vypnuta a poté znovu zapnuta, ikony chyby plánování se mohou zobrazit v WBS. 

**Oprava chyb plánování dle úkolu** Pokud dvakrát kliknete na ikonu chyby plánu pro konkrétní úkol, zobrazí dialogové okno všechny chyby plánování pro tento úkol. Můžete určit, které chyby plánování chcete pro úkol opravit. 

**Oprava všech chyb plánování** Pokud chcete, aby aplikace Finance and Operations opravila všechny chyby plánování ve WBS, v podokně akcí klikněte na možnost **Opravit všechny nesrovnalosti plánování**. 

> [!NOTE] 
> Tato funkce může způsobit výrazné úpravy struktury WBS. Chyby budou opraveny v následujícím pořadí:

1.  Odhadované úsilí na všechny úkoly je upraveno tak, aby se rovnalo hodnotě kapacity, která je definována v projektovém kalendáři.
2.  Počáteční datum každého úkolu je změněno tak, aby byl úkol zahájen až po dokončení všech jeho předchůdců.
3.  Počáteční datum jednotlivých úkolů se mění tak, aby zmizely mezery mezi počátečními daty předchozích úkolů.

### <a name="cost-estimation"></a>Odhad nákladů

Jako bylo uvedeno výše v tomto dokumentu, zadejte odhad nákladů pro každý úkol listového uzlu pomocí karty **Odhadované náklady a výnosy** v dolním podokně stránky **Strukturovaný rozpis prací**. 

> [!NOTE] 
> Odhad nákladů pro úkol souhrnu nebo kontejneru nelze změnit. Odhad nákladů pro souhrnný úkol se rovná součtu odhadu nákladů úkolů jeho listového uzlu. Celkové odhadované náklady pro každý úkol se vypočítají jako součet částek odhadovaných nákladů pro následující typy transakcí:

-   Práce
-   Zboží nebo materiál
-   Výdaje

Typ transakce **Poplatek** se používá pro odhad výnosů na základě poplatků. Tento typ transakce nemá komponentu nákladů a není proto při odhadu nákladů zahrnut. 

Typ transakce **Akontace** se používá k záznamu smluvní prodejní hodnoty u typu projektu s pevnou hodnotou. Tento typ transakce se rovněž nebere v potaz při odhadu nákladů. 

Při odhadu nákladů na práci, materiál a výdaje pro každý úkol je nutné přiřadit kategorii projektu k odhadovaným nákladům. 

**Odhad nákladů na práci** Pro každý úkol listového uzlu přiřadíte pracovní úsilí v hodinách a výchozí kategorii. Z toho vyplývá, že když nastavujete plán pro úkol, odhad nákladů na práci pro daný úkol bude automaticky přidán do výchozí kategorie pro práci. Tento odhad nákladů se zobrazí na kartě **Odhadované náklady a výnosy** v mřížce **Podrobnosti řádku** pro tento úkol. Pokud potřebujete další odhady nákladů práce, můžete je přidat na této kartě. Pokud zvýšíte nebo snížíte počet hodin odhadu nákladů práce, plán úlohy se automaticky přepočítá. 

**Odhad výdajů a nákladů na materiál** Karta **Odhadované náklady a výnosy** také umožňuje odhadnout výdaje a náklady na materiál pro úkol, pokud potřebujete odhady. 

Náklady a prodejní cena pro každý řádek odhadu práce nebo výdajů vycházejí z nastavení, které je definováno pro každou kategorii v tabulkách cen v nabídce **Řízení a účetnictví projektů** &gt; **Nastavení** &gt; **Oceňování**. Pro zboží jsou ceny a prodejní ceny přidány ve výchozím nastavení ze smluv o zboží nebo obchodních smluv na stránce seznamu **Uvolněné produkty** v modulu řízení informací o produktu.

## <a name="tracking-progress-on-the-wbs"></a>Sledování průběhu struktury WBS
Některá odvětví sledují průběh projektu proti WBS na velmi podrobné úrovni, zatímco jiná sledují průběh na vyšší úrovni struktury WBS. Tato část popisuje použití sledování WBS pro požadavky projektu. 

Aplikace Finance and Operations obsahuje tři zobrazení struktury WBS projektu: zobrazení plánování, zobrazení sledování úsilí a zobrazení sledování nákladů.

### <a name="planning-view"></a>Zobrazení plánování

Zobrazení plánování zobrazuje plánovaný nebo základní odhad informací o plánu a nákladech. I když nejsou k dispozici žádné funkce ke sledování verze a základu struktury WBS projektu, hodnoty v tomto zobrazení mají představovat základní verzi. Oddíly Odhad plánu a Odhad nákladů v tomto tématu popisují toto zobrazení a jeho použití k vytvoření struktury WBS.

### <a name="effort-tracking-view"></a>Zobrazení sledování úsilí

Zobrazení sledování úsilí zobrazuje sledování průběhu úkolů ve WBS. Porovnává celkové skutečné úsilí (počet hodin) s plánovanými hodinami úsilí. Následující vzorce poskytují hodnoty v zobrazení sledování úsilí:

-   Procenta průběhu = Skutečné úsilí k datu ÷ Plánované úsilí úkolu
-   Zbývající úsilí (neboli odhad k dokončení \[ETC\]) = Plánované úsilí – Skutečné úsilí k datu
-   Odhad při dokončení (EAC) = Zbývající úsilí + Skutečné úsilí k datu
-   Předpokládané odchylky úsilí = Plánované úsilí – EAC

Zobrazení sledování úsilí zobrazuje předpoklad odchylky úsilí pro daný úkol podle toho, zda je EAC vyšší nebo nižší než plánované úsilí:

-   Pokud je EAC vyšší než plánované úsilí, očekává se, že úkol bude trvat déle, než bylo původně plánováno, a je pozadu za plánem.
-   Pokud je EAC nižší než plánované úsilí, očekává se, že úkol bude trvat kratší dobu, než bylo původně plánováno, a je před plánem.

**Opětovný předpoklad úsilí manažerem projektu** Občas bude muset manažer projektu nebo jiná osoba, která sleduje průběh projektu, revidovat původní odhady úkolu. Úkol může probíhat rychleji nebo pomaleji, než se původně očekávalo, a to z různých důvodů. Například byl snížen jeho rozsah nebo pracovníci mají menší zkušenosti, než bylo původně v plánu. Předpoklady jsou tím, jak manažer projektu vnímá odhady, na základě aktuálního stavu projektu. Obecně platí, že byste neměli měnit základní čísla, protože základ projektu představuje řádně publikovaný dokument pro plán projektu a odhad nákladů, na kterém se dohodli všichni účastníci projektu. 

Vedoucí projektu může změnit úsilí na úkolech dvěma způsoby:

-   Upravte zbývající úsilí, které je nastaveno automaticky, tak, aby se skutečné zbývající úsilí u daného úkolu aktualizovalo.
-   Upravte procenta průběhu, které je nastaveno automaticky, tak, aby se skutečný průběh daného úkolu aktualizoval.

Oba tyto přístupy způsobují přepočet ETC, EAC a procenta průběhu a předpokládanou odchylku úsilí úkolu. EAC, ETC a procento průběhu souhrnných úkolů rovněž budou přepočteny a jejich předpokládaná odchylka úsilí se aktualizuje. 

**Upravené úsilí u souhrnných úkolů** Je možné změnit úsilí úkolů souhrnu nebo kontejneru. Bez ohledu na to, zda upravíte tyto hodnoty pomocí zbývající úsilí nebo procenta průběhu pro souhrnné úkoly, výpočty se automaticky objeví v následujícím pořadí:

1.  Vypočítáno bude EAC, ETC a procento průběhu úkolu.
2.  Nový EAC je mezi podřazené úkoly rozdělen ve stejném poměru jako původní částky EAC.
3.  Vypočte se nový EAC na jednotlivé úkoly listového uzlu.
4.  Zbývající úsilí a procento dokončení bude přepočítáno pro všechny podřízené ovlivněné úkoly na základě nové hodnoty EAC. Rovněž bude přepočtena odchylka úsilí úkolů.
5.  EAC souhrnných úkolů z listového uzlu bude také přepočítána.

Kliknutím na tlačítko **Rozšířit na úroveň** v zobrazení sledování úsilí nastavte úroveň, ve které chcete sledovat a spravovat WBS. Struktura WBS je automaticky rozšířena na danou úroveň při každém otevření v zobrazení sledování úsilí.

### <a name="cost-tracking-view"></a>Zobrazení sledování nákladů

Zobrazení sledování nákladů zobrazuje sledování spotřeby nákladů pro úkol. V tomto zobrazení jsou porovnány skutečné náklady utracené za úkol k danému datu a plánované náklady pro daný úkol. Následující vzorce poskytují hodnoty v zobrazení sledování nákladů:

-   Procento spotřebovaných nákladů = Skutečné náklady k datu ÷ Plánované náklady pro úkol
-   Náklady na dokončení (CTC) = Plánované náklady – Skutečné náklady k datu
-   Odhad při dokončení (EAC) = CTC + Skutečné náklady k datu
-   Předpokládané odchylky nákladů = Plánované náklady – EAC

Zobrazení sledování nákladů zobrazuje předpoklad odchylky nákladů pro daný úkol podle toho, zda je EAC vyšší nebo nižší než plánované náklady:

-   Pokud je EAC vyšší než plánované náklady, očekává se, že úkol bude stát více, než bylo původně plánováno, a přesahuje rozpočet.
-   Pokud je EAC nižší než plánované náklady, očekává se, že úkol bude stát méně, než bylo původně plánováno, a nedosahuje rozpočtu.

**Opětovný předpoklad nákladů manažerem projektu** Manažeři projektu musí použít CTC k revizi původního odhadu nákladů na úkol. Manažer projektu může upravit hodnotu CTC na náklady, které jsou nutné k dokončení úkolu. Jestliže změníte hodnotu CTC, pak bude přepočítána hodnota CTC, EAC a procento spotřebovaných nákladů úkolu a předpokládaná odchylka nákladů na úkol. EAC, ETC a procento nákladů spotřebovaných na souhrnné úkoly rovněž budou přepočteny a jejich předpokládaná odchylka nákladů se aktualizuje. 

> [!NOTE] 
> Při změně úsilí úkolu struktury WBS v zobrazení sledování úsilí budou hodnoty CTC, EAC a procento spotřebovaných nákladů na úkol a předpokládaná odchylka nákladů přepočteny v zobrazení sledování nákladů. Revize nákladů však neovlivňují hodnoty v zobrazení sledování úsilí, vzhledem k tomu, že nejsou revidovány náklady dle typu transakce (práce, materiál nebo výdaje) nebo kategorie projektu. 

**Revize předpokladu nákladů na souhrnné úkoly** Je možné revidovat náklady na souhrnné úkoly a výpočty se automaticky objeví v následujícím pořadí:

1.  Přepočítají se hodnoty EAC, CTC a procento spotřebovaných nákladů na úkol.
2.  Nový EAC je mezi podřazené úkoly rozdělen ve stejném poměru jako původní EAC v úkolech.
3.  Bude vypočten nový EAC pro každý úkol.
4.  CTS a procento spotřebovaných nákladů bude přepočteno pro dotčené podřízené úkoly, na základě hodnoty EAC. Rovněž bude přepočtena odchylka nákladů na úkoly.
5.  EAC pro všechny souhrnné úkoly se přepočítávají podle této změny.

Kliknutím na tlačítko **Rozšířit na úroveň** v zobrazení sledování nákladů nastavte úroveň, ve které chcete sledovat a spravovat WBS. Struktura WBS je rozšířena na danou úroveň při každém otevření v zobrazení sledování nákladů.

### <a name="earned-value-management"></a>Správa získané hodnoty

Metodu získané hodnoty (EVM) můžete použít ke sledování průběhu projektu. Metriky získané hodnoty zobrazíte na pracovní ploše role vedoucího projektu. Komponenta grafu získané hodnoty obsahuje hodnoty časového uspořádání plánované hodnoty a skutečných nákladů. Získaná hodnota k aktuálnímu datu je zobrazena jako bod. Data časového uspořádání získané hodnoty nyní nejsou k dispozici. 

Fáze času v grafu získané hodnoty se zobrazí podle týdne nebo měsíce. Tato část popisuje tři pilíře systému EVM: plánovaná hodnota, získaná hodnota a skutečné náklady. 

**Plánovaná hodnota** Teorie systému EVM uvádí, že vykreslení plánované hodnoty představuje míru, s jakou tým projektu plánoval získat hodnotu projektu. 

Finance and Operations používá pravidlo zisku 0:100 při vykreslování plánované hodnoty. Podle tohoto pravidla je hodnota úkolu zaúčtována do úkolu k datu ukončení. Žádná hodnota nebude zaúčtována, dokud nebude úkol 100procentně dokončen. 

V modulu Řízení a účetnictví projektů zadejte koncové datum listových uzlů a plánované náklady pro ně. Při zobrazení grafu plánované hodnoty dle týdnů jsou plánované hodnoty shrnuty za týden pro všechny úlohy listového uzlu pro dobu trvání projektu. 

**Získaná hodnota** Teorie systému EVM uvádí, že vykreslení získané hodnoty představuje míru, s jakou tým projektu skutečně získá hodnotu projektu. 

Finance and Operations používá pravidlo zisku 0:100 při vykreslování získané hodnoty. Podle tohoto pravidla je hodnota úkolu zaúčtována do úkolu k datu ukončení. Žádná hodnota nebude zaúčtována, dokud nebude úkol 100procentně dokončen. 

Při výpočtu získané hodnoty je zvažováno procento průběhu jednotlivých úkolů. Podle pravidla zisku 0:100 budou do výpočtu získané hodnoty na konci období zahrnuty pouze úkoly, které byly dokončeny v daném období. Získaná hodnota projektu se vypočítá pro všechny úkoly, které již byly dokončeny při vytvoření grafu. 

> [!NOTE] 
> V současné době systém sledování WBS neobsahuje datové struktury pro uložení historických procentuálních hodnot jednotlivých úkolů. Získaná hodnota tedy může být vykazována pouze k času zpracování datové krychle. Krychli zpracovávejte pravidelně, aby bylo možné aktualizovat data získané hodnoty, která jsou zobrazena na pracovní ploše role. 

**Skutečné náklady** Teorie systému EVM uvádí, že vykreslení skutečných nákladů představuje míru, se kterou jsou peníze na projekt využity. 

Transakce, které jsou zaúčtovány v projektu, jsou použity k vykreslení řádku skutečných nákladů. Náklady jsou uvedeny souhrnně podle data. Tyto údaje jsou pak použity k vytvoření grafu získané hodnoty skutečných nákladů dle týdne nebo měsíce.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Použití konceptů plánované hodnoty, získané hodnoty a skutečných nákladů

**Odchylka plánu** Během plánování vytvoříte prognózu pro práci na časové ose. Plánovaná hodnota je tedy míra, se kterou plánovači projektu předpokládali, že bude práce na projektu dokončena. V průběhu projektu je práce dokončena a projekt získá hodnotu. Porovnáním plánované hodnoty a získané hodnoty lze zobrazit, jak práce v projektu probíhá. Výsledek tohoto porovnání se nazývá odchylka plánu. 

Je-li plánovaná hodnota pro období vyšší než získaná hodnota, množství práce, která byla provedena v projektu, je nižší, než co bylo plánováno. Projekt je tedy pozadu za plánem. Vzhledem k tomu, že plánovaná hodnota a získaná hodnota je vyjádřena v peněžních pojmech, prodleva projektu je také uvedena jako peněžní hodnota. 

Je-li plánovaná hodnota pro období nižší než získaná hodnota, množství práce, která byla provedena v projektu, je vyšší, než co bylo plánováno. Projekt je tedy před plánem. Této době realizace je rovněž přiřazena peněžní hodnota.

**Odchylka nákladů** Vzhledem k tomu, že získaná hodnota používá nákladovou cenu jako koeficient, získaná hodnota označuje náklady na práci, která se provádí v projektu. V průběhu projektu jsou do transakčního protokolu zaznamenávány finance, které byly na projekt skutečně vydány. Porovnáním získané hodnoty se skutečnými náklady můžete zobrazit vydaný peněžní obnos a získanou hodnotu. Výsledek tohoto porovnání se nazývá odchylka nákladů. 

Pokud jsou skutečné náklady, které byly vydány v daném období, vyšší než získaná hodnota, bylo utraceno více peněz, než bylo získáno. Projekt tedy překračuje rozpočet. 

Pokud jsou skutečné náklady, které byly vydány v daném období, nižší než získaná hodnota, bylo získáno více peněz, než bylo utraceno. Projekt tedy nedosahuje rozpočtu.

## <a name="wbs-templates"></a>Šablony WBS
Funkce šablon WBS můžete použít k vytvoření standardních šablon pro projekty. Pokud projekty, které vaše společnost nabízí, zahrnují mnoho opakovatelných úkolů, zvažte vytvoření šablony WBS. 

Vytvořte šablonu WBS ze struktury WBS existujícího projektu, aby znalosti a doporučené postupy, které získáte během plánování projektu, bylo možné znovu použít v podobných projektech v budoucnosti. V některých případech však nemusí smysl uložit celou strukturu WBS jako šablonu. Proto můžete také vytvořit šablony z částí struktury WBS pro projekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Uložení struktury WBS projektu jako šablony

Po vytvoření šablony ji můžete importovat do nové struktury WBS projektu pod kořenovým uzlem nebo pod všemi úkoly ve strukturách WBS projektu.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Import šablony WBS do struktury WBS projektu

Při importu úkolů jsou úkoly v šabloně uspořádány podle počátečního data úkolu, pod kterým jsou importovány. Během importu se vztahy předcházejících úkolů v šabloně používají k výpočtu data zahájení pro importované úkoly. Standardní pracovní kalendář cílového projektu se použije k výpočtu koncových dat importovaných úkolů tak, že budou zachovány pracovní dny a standardní pracovní doby, které jsou definovány v pracovním kalendáři aktuálního projektu. 

Částky nákladů a prodejní ceny pro řádky odhadu jsou použity k zajištění, že ceny specifické pro projekt nebo projektovou smlouvu mají platná data.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Rozdíly mezi strukturou WBS projektu a šablonou WBS

-   Úkoly v šablonách WBS nemají počáteční a koncové datum.

Šablony a nepracovní dny nejsou nastaveny pro šablony WBS.

-   Šablony WBS vždy používejte plánovací kalendář, který je nastaven jako výchozí kalendář pro všechny projekty.

Výchozí plánovací kalendář se používá pouze ke zjištění hodin ve standardním pracovním dni.

-   Vztahy předchůdců nejsou zkopírovány do šablony WBS.

Vzhledem k tomu, že šablony WBS nemají data, není nutné použít logiku počátečního data založenou na koncovém datu předchůdce.

-   Řádek odhadu nákladů na práci je vytvořen automaticky při vytvoření úkolu v šabloně struktury WBS. Prodejní cena a částka nákladů bude zkopírována z vybraného pracovníka.

Výdaje a náklady na zboží lze vytvořit ručně, stejně jako je tomu u struktury WBS projektu.

-   Chyby plánování se zobrazí, pokud vzniknou odchylky od následujícího vzorce:

Úsilí = počet zdrojů × × doba trvání × počet hodin ve standardní pracovní den 

Klepnutím na **Opravit všechny chyby plánování** můžete opravit všechny chyby plánování současně. 

Případně můžete opravit chyby plánování jednotlivě, kliknutím na ikonu upozornění pro jednotlivé úkoly.



