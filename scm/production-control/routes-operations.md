---
title: "Postupy a operace"
description: "Toto téma obsahuje obecné informace o postupech a operacích. Postup definuje proces pro výrobu produktu nebo varianty produktu. Popisuje jednotlivé kroky (operace) ve výrobním procesu a pořadí, ve kterém je nutné je provádět. U každého kroku postup také definuje požadované provozní prostředky, čas, který je nutný k přípravě a provedení operace, a způsob výpočtu nákladů."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7193e3aeac651effe64877c607fc76eef8782731
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="routes-and-operations"></a>Postupy a operace

[!include[banner](../includes/banner.md)]


Toto téma obsahuje obecné informace o postupech a operacích. Postup definuje proces pro výrobu produktu nebo varianty produktu. Popisuje jednotlivé kroky (operace) ve výrobním procesu a pořadí, ve kterém je nutné je provádět. U každého kroku postup také definuje požadované provozní prostředky, čas, který je nutný k přípravě a provedení operace, a způsob výpočtu nákladů.

<a name="overview"></a>Přehled
--------

Postup popisuje pořadí operací při výrobě produktu nebo varianty produktu. U každé operace postup také definuje požadované provozní prostředky, čas, který je nutný k nastavení a provedení operace, a způsob výpočtu nákladů. Stejný postup lze použít k výrobě více produktů nebo můžete definovat jedinečný postup pro každý produkt či variantu produktu. Můžete používat i více postupů pro stejný produkt. V takovém případě konkrétní použitý postup závisí na různých faktorech, jako je vyráběné množství. Definice postupu v aplikaci Microsoft Dynamics 365 for Operations se skládá ze čtyř samostatných prvků, které společně popisují výrobní proces:

-   **Postup** – definuje strukturu výrobního procesu. Jinými slovy určuje pořadí operací.
-   **Operace** – určuje konkrétní pojmenovaný krok v postupu, například **Sestavení**. Stejná operace se může vyskytovat v několika různých postupech a může mít přiřazena různá čísla.
-   **Vztah operace** – definuje provozní vlastnosti operace, například čas nutný k přípravě a provedení operace, nákladové kategorie, parametry spotřeby a požadavky na prostředky. Pomocí vztahů operací lze provozní vlastnosti operací měnit podle postupu, ve kterém se operace používá, nebo produktů, které se vyrábějí.
-   **Verze postupu** – definuje postup, který se používá k výrobě produktu nebo varianty produktu. Verze postupů umožňují průběžné úpravy nebo opakované používání postupů u různých produktů. Umožňují také použití různých postupů k výrobě stejného produktu. V takovém případě konkrétní použitý postup závisí na různých faktorech, jako je místo nebo vyráběné množství.

## <a name="routes"></a>Postupy
Postup popisuje pořadí operací při výrobě produktu nebo varianty produktu. Každé operaci se přiřadí číslo a následná operace. Pořadí operací tvoří síťový postup, který lze znázornit pomocí diagramu s jedním nebo několika počátečními body a jedním koncovým bodem. V aplikaci Dynamics 365 for Operations se postupy rozlišují podle typu struktury. Existují dva typy postupů: jednoduché postupy a síťové postupy. Ve formuláři Parametry modulu Řízení výroby můžete určit, zda lze použít pouze jednoduché postupy nebo i složitější síťové postupy.

### <a name="simple-routes"></a>Jednoduché postupy

Jednoduchý postup je sekvenční a existuje u něj pouze jeden počáteční bod.  

[![Jednoduchý postup](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Pokud ve formuláři Parametry modulu Řízení výroby povolíte pouze jednoduché postupy, aplikace Dynamics 365 for Operations při definování postupu automaticky vygeneruje čísla operací (10, 20, 30 a tak dále).

### <a name="route-networks"></a>Síťové postupy

Pokud ve formuláři Parametry modulu Řízení výroby povolíte složitější síťové postupy, můžete definovat postupy, které mají více počátečních bodů, a operace, které lze spustit současně.  

[![Síťový postup](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Poznámky:**

-   Každá operace může mít pouze jednu následnou operaci a celý postup musí končit jednou operací.
-   Neexistuje žádná záruka, že více operací, které mají stejnou následnou operaci (například operace 30 a 40 na předchozím obrázku), budou skutečně probíhat souběžně. Dostupnost a kapacita prostředků může omezovat plánování operací.
-   Jako číslo operace nelze použít hodnotu 0 (nula). Toto číslo je rezervováno a slouží k určení skutečnosti, že poslední operace v postupu nemá žádné následné operace.

### <a name="parallel-operations"></a>Paralelní operace

Někdy je k provedení operace třeba kombinace několika provozních prostředků s odlišnými vlastnostmi. Operace montáže může například vyžadovat stroj, nástroj a jednoho dohlížejícího pracovníka u každých dvou strojů. Tento příklad lze modelovat pomocí paralelních operací, kde je jedna operace určena jako primární operace a ostatní jsou sekundární.  

[![Postup s primární operací a sekundárními operacemi](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Primární operace obvykle představuje kritický prostředek a určuje dobu nutnou k provedení sekundárních operací. Při plánování s omezenou kapacitou však musí být k dispozici prostředky, které jsou naplánovány pro primární i sekundární operace, a současně musí mít volnou kapacitu.  

Primární i sekundární operace musí mít stejné číslo operace (30 na předchozím obrázku).  

V předchozím příkladu je požadavkem na prostředek u primární operace (30) stroj, zatímco u sekundárních operací (30' a 30'') se jedná o nástroj a pracovníka. Díky 50% vytížení lze zajistit, aby pracovník mohl dohlížet na dva stroje současně.

### <a name="approval-of-routes"></a>Schválení postupů

Každý postup je před použitím v plánovacím nebo výrobním procesu nutné schválit. Schválení znamená, že návrh postupu byl dokončen. Stejné uvolněné produkty nebo varianty produktu mohou mít více schválených postupů. Schválení postupu obvykle proběhne při schválení první relevantní verze postupu. U některých obchodních scénářů představují schválení postupu a verze postupu samostatné aktivity, do kterých mohou být zapojeni různí vlastníci procesů.  

Každý postup lze schválit nebo zamítnout samostatně. Při zamítnutí postupu však budou zamítnuty i všechny související verze postupu. Ve formuláři Parametry modulu Řízení výroby lze určit, zda je možné postupy zamítnout a zda je možné měnit schválené postupy.  

Pokud potřebujete uchovávat záznamy o tom, kdo jednotlivé postupy schvaluje, můžete si při jejich schvalování vyžádat elektronické podpisy. V takovém případě musí uživatelé [elektronickým podpisem](/dynamics365/operations/organization-administration/electronic-signature-overview) potvrzovat svou identitu.

## <a name="operations"></a>Operace
Operace představuje krok ve výrobním procesu. V aplikaci Dynamics 365 for Operations má každá operace ID a jednoduchý popis. Následující tabulka ukazuje typické příklady operací ze strojní dílny.

| Operace  | Popis        |
|------------|--------------------|
| PipeCut    | Řezání potrubí       |
| TIGweld    | Svařování TIG        |
| JigAssy    | Montáž       |
| Inspection | Kontrola kvality |

Provozní vlastnosti operace, například čas nutný k přípravě a provedení operace, požadavky na prostředky, informace o nákladech a výpočty spotřeby, jsou uvedeny ve vztahu operace. (Další informace o vztazích operací naleznete v další části.)

## <a name="operation-relations"></a>Vztahy operací
Ve vztahu operace se uchovávají následující provozní vlastnosti operace:

-   Nákladové kategorie
-   Parametry spotřeby
-   Čas zpracování
-   Zpracovávané množství
-   Požadavky na prostředek
-   Poznámky a pokyny

Pro jednu operaci můžete definovat více vztahů operace. Každý vztah operace však platí pro jednu konkrétní operaci a obsahuje vlastnosti, které jsou specifické pro postup, uvolněný produkt nebo sadu uvolněných produktů, které se vztahují ke skupině položek. Stejné operace lze tedy použít v několika postupech, které mají různé provozní vlastnosti. Pokud použijete standardní operace, které mají stejné provozní vlastnosti, budete moci snáze udržovat hlavní data (bez ohledu na používaný postup a vyráběný produkt). Rozsah vztahu operace je definován pomocí vlastností **Kód položky**, **Vztah položky**, **Kód postupu** a **Vztah postupu**, jak je znázorněno v následující tabulce.

| Kód položky | Vztah položky         | Kód postupu | Vztah postupu   | Rozsah vztahu operace                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabulka     | &lt;ID položky&gt;       | Postup      | &lt;ID postupu&gt; | Provozní vlastnosti operace použité v postupu (kde **Číslo postupu**=&lt;ID postupu&gt;) k výrobě uvolněného produktu, kde **Číslo položky**=&lt;ID položky&gt;.                                                                                                                        |
| Tabulka     | &lt;ID položky&gt;       | Vše        |                  | Výchozí provozní vlastnosti operace použité k výrobě uvolněného produktu, kde **Číslo položky**=&lt;ID položky&gt;. Jinými slovy – tyto provozní vlastnosti platí, pokud u uvolněného produktu neexistuje žádný vztah operace, který je specifický pro daný postup.                                     |
| Seskupit     | &lt;ID skupiny položek&gt; | Postup      | &lt;ID postupu&gt; | Provozní vlastnosti operace použité v postupu (kde **Číslo postupu**=&lt;ID postupu&gt;) k výrobě uvolněných produktů spojených se skupinou položek (&lt;ID skupiny položek&gt;), pokud u uvolněného produktu neexistuje vztah operace specifický pro daný postup.                         |
| Seskupit     | &lt;ID skupiny položek&gt; | Vše        |                  | Výchozí provozní vlastnosti operace použité k výrobě uvolněných produktů spojených se skupinou položek &lt;ID skupiny položek&gt;, pokud neexistuje konkrétnější vztah operace.                                                                                                  |
| Vše       |                       | Postup      | &lt;ID postupu&gt; | Výchozí provozní vlastnosti operace použité v postupu, kde **Číslo postupu**=&lt;ID postupu&gt;. Jinými slovy – tyto provozní vlastnosti platí, pokud u daného postupu neexistuje žádný vztah operace, který je specifický pro uvolněný produkt nebo související skupinu položek. |
| Vše       |                       | Vše        |                  | Výchozí provozní vlastnosti operace. Tyto provozní vlastnosti platí, pokud neexistuje konkrétnější vztah operace.                                                                                                                                                                |

Můžete také určit, že vztah operace bude platit jen pro konkrétní pracoviště. Provozní vlastnosti operace se tak mohou lišit podle místa (tedy pracoviště), kde se operace provádí. U konfigurovaných produktů můžete také určit různé provozní vlastnosti pro každou konfiguraci produktu.  

Vztahy operací zajišťují při definici postupů velkou flexibilitu. Možnost definovat výchozí vlastnosti navíc pomáhá snižovat množství hlavních dat, která je nutné uchovávat. Tato flexibilita však také znamená, že si musíte být vědomi kontextu, ve kterém vztahy operací upravujete.  

**Poznámka:** Provozní vlastnosti jsou uloženy ve vztazích operací u každé operace a každého postupu a všechny výskyty stejné operace (například montáže) mají stejný přípravný a operační čas, požadavky na prostředky a podobně. Pokud se tedy dva výskyty operace musí nacházet ve stejném postupu, ale mají různé operační časy, je nutné vytvořit dvě samostatné operace, například Montáž1 a Montáž2.

### <a name="modifying-product-specific-routes"></a>Změna postupů u konkrétních produktů

Po otevření stránky **Postup** na stránce **Podrobnosti o uvolněném produktu** se zobrazí verze postupu spojené s vybraným uvolněným produktem. V tomto kontextu u každé operace aplikace Dynamics 365 for Operations zobrazuje provozní vlastnosti ze vztahu operace, který co nejlépe odpovídá verzi postupu. Seznam operací obsahuje vlastnosti **Kód položky** a **Kód postupu** ze vztahu operace. Je tedy možné určit, který vztah operace se zobrazuje.  

Na stránce **Postup** můžete změnit provozní vlastnosti operace, například operační čas nebo nákladové kategorie. Provedené změny se uloží do vztahu operace specifického pro postup a uvolněný produkt, na které se aktuální verze postupu odkazuje. Pokud zobrazený vztah operace není specifický pro daný postup a uvolněný produkt, systém před uložením změn vytvoří jeho kopii. Tato kopie *je* specifická pro daný postup a uvolněný produkt. Její změny tedy neovlivní jiné postupy nebo uvolněné produkty. Chcete-li si ověřit, který vztah operace se na stránce **Postup** upravuje, podívejte se na pole **Kód položky** a **Kód postupu**.  

Operaci, která je specifická pro daný postup a uvolněný produkt, můžete také ručně vytvořit pomocí funkce **Kopírovat a upravit vztah**.  

**Poznámka:** Pokud k postupu přidáte novou operaci na stránce **Postup**, vztah operace se vytvoří pouze pro aktuální uvolněný produkt. Jestliže tedy postup slouží také k výrobě jiných uvolněných produktů, nebude pro ně existovat žádný platný vztah operace a postup nebude pro tyto uvolněné produkty možné dále používat.

### <a name="maintaining-operation-relations-per-route"></a>Udržování vztahů operací u jednotlivých postupů

Při otevření stránky **Podrobnosti postupu** ze stránky seznamu **Postupy** se zobrazí seznam všech vztahů operací, které platí pro vybraný postup. Pomocí něj lze snadno ověřit, které provozní vlastnosti se používají pro jednotlivé produkty. Můžete upravit výchozí hodnoty vlastností i hodnoty vlastností specifické pro daný produkt.  

Když přidáte nový vztah operace na stránce **Podrobnosti postupu**, pole **Kód postupu** se automaticky nastaví na hodnotu **Postup** a pole **Vztah postupu** pole se nastaví na číslo aktuálního postupu.

### <a name="maintaining-operation-relations-per-operation"></a>Udržování vztahů operací u jednotlivých operací

Na stránce **Operace** můžete otevřít stránku **Vztahy operací**. Na této stránce můžete upravit všechny vztahy určité operace. Je možné upravit i vztahy operací, které obsahují výchozí hodnoty.  

Pokud váš podnik používá standardní operace a provozní parametry jsou u všech produktů a procesů stejné, můžete pomocí stránky **Vztahy operací** pohodlně spravovat výchozí provozní vlastnosti těchto operací.

### <a name="applying-operation-relations"></a>Používání vztahů operací

V některých případech musí aplikace Dynamics 365 for Operations najít provozní vlastnosti operace. Například při vytvoření nákupní objednávky je třeba zkopírovat provozní vlastnosti každé operace ze vztahů operací do výrobního postupu. V těchto situacích aplikace Dynamics 365 for Operations hledá příslušné vztahy operací od nejkonkrétnější k nejméně konkrétní kombinaci.  

Když aplikace Dynamics 365 for Operations hledá nejrelevantnější vztah operace u uvolněného produktu, upřednostňuje přitom vztah, který odpovídá ID položky uvolněného produktu, před vztahem, který odpovídá ID skupiny položek. Vztah operace, který odpovídá ID skupiny položek, má zase přednost před výchozím vztahem operace. Hledání se provádí v tomto pořadí:

1.  **Kód položky**=**Tabulka** a **Vztah položky**=&lt;ID položky&gt;
2.  **Kód položky**=**Skupina** a **Vztah položky**=&lt;ID skupiny položek&gt;
3.  **Kód položky**=**Vše**
4.  **Kód postupu**=**Postup** a **Vztah postupu**=&lt;ID postupu&gt;
5.  **Kód postupu**=**Vše**
6.  **Konfigurace**=&lt;ID konfigurace&gt;
7.  **Konfigurace**=
8.  **Pracoviště**=&lt;ID pracoviště&gt;
9.  **Pracoviště**=

Každá operace by se tedy měla v každém postupu použít jen jednou. Pokud se ve stejném postupu vyskytuje vícekrát, budou všechny její výskyty mít stejný vztah operace a u jednotlivých výskytů nebude možné nastavit různé vlastnosti (například operační časy).

## <a name="route-versions"></a>Verze postupu
Verze postupů se používají pro zohledňování odlišností při výrobě produktů nebo k zajištění větší kontroly nad výrobním procesem. Určují, který postup se má použít při výrobě konkrétního uvolněného produktu nebo varianty produktu. Při určování postupu použitého pro uvolněný produkt můžete použít následující omezení:

-   Dimenze produktu (velikost, barva, styl nebo konfigurace)
-   Vyráběné množství
-   Výrobní pracoviště
-   Datum výroby

Pokud vyrábíte produkt na konkrétním pracovišti či v určitém množství nebo období, je možné označit některou konkrétní verzi postupu jako výchozí. Mějte však na paměti, že u každého uvolněného produktu a příslušných omezení je povolen pouze jeden aktivní postup.  

Ve formuláři Parametry modulu Řízení výroby lze určit, že musí být vždy zadána doba platnosti verze postupu.

### <a name="approval-of-route-versions"></a>Schvalování verzí postupů

Každou verzi postupu je před použitím v plánovacím nebo výrobním procesu nutné schválit. Když verzi postupu schválíte, můžete schválit i související postup. Verzi postupu je však možné schválit jen v případě, že je schválen i související postup.

### <a name="activating-the-default-route-version"></a>Aktivace výchozí verze postupu

Aktivací verze postupu ji označíte jako výchozí verzi, kterou bude používat hlavní plánování nebo která bude sloužit k vytváření výrobních zakázek. U každé sady omezení (například období, pracoviště nebo množství) je možné používat pouze jednu aktivní verzi postupu. Pokud je verze, kterou se pokoušíte aktivovat, v konfliktu s již aktivní verzí, zobrazí se chybová zpráva. V takovém případě je třeba deaktivovat konfliktní verzi nebo upravit omezení verze (obvykle období), aby nedošlo k nejednoznačné aktivaci.

### <a name="electronic-signatures"></a>Elektronické podpisy

Pokud potřebujete uchovávat záznamy o tom, kdo jednotlivé verze postupů schvaluje a aktivuje, můžete si u těchto úkonů vyžádat elektronické podpisy. Uživatelé, kteří schvalují a aktivují verze postupů, pak budou muset potvrzovat svou identitu pomocí [elektronického podpisu](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Změna produktu s využitím správy případu

Pomocí případu změny produktu týkajícího se schválení a aktivace nových nebo změněných postupů a verzí postupů můžete snadno získat informace o omezeních verze postupu. Můžete také schválit a aktivovat všechny postupy, které souvisí s určitou změnou v jedné operaci, a zdokumentovat výsledky v případu změny produktu.

## <a name="maintaining-routes"></a>Udržování postupů
Podle toho, jaké jsou požadavky vašeho podnikání, se vám může podařit zredukovat množství práce nutné k údržbě definic procesů.

### <a name="making-routes-independent-of-resources"></a>Vytváření postupů nezávislých na prostředcích

U mnoha systémů je v postupu nutné určit provozní prostředek nebo skupinu prostředků, které mají provádět operace. V aplikaci Dynamics 365 for Operations však lze definovat požadavky, které musí provozní prostředek splňovat, aby ho bylo možné při operaci použít. Konkrétní provozní prostředky nebo skupiny prostředků, které se mají použít, tedy není nutné určovat, dokud nebude operace ve skutečnosti naplánována. Tato funkce je užitečná zvláště v případě, že máte k dispozici mnoho strojů pracovníků, kteří mohou provádět stejnou operaci.  

Můžete například určit, že operace vyžaduje provozní prostředek typu **Stroj**, který má funkci **Lisování** s kapacitou 20 tun. Plánovací modul pak při plánování operace podle těchto požadavků vybere konkrétní provozní prostředek nebo skupinu prostředků. Díky tomu, že stačí zadat pouze tyto požadavky a není nutné spojovat celou operaci s konkrétním strojem, máte mnohem větší flexibilitu. Údržba při přesouvání nebo přidávání nových prostředků je navíc snazší.  

Další informace o různých typech požadavků na prostředky a jejich použití naleznete v tématu Požadavky na prostředky u operací a [Schopnosti prostředku](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Sdílení postupů mezi pracovišti

Pokud vyrábíte stejný produkt na více pracovištích a výrobní postupy jsou všude stejné, můžete vytvořit sdílený postup, který se použije na všech pracovištích. Chcete-li takový sdílený postup vytvořit, nezadávejte pracoviště přímo u použitého postupu. Je třeba vytvořit verzi postupu, která přidruží sdílený postup k produktu na každém pracovišti.  

Je také nutné zajistit, aby jednotlivé operace nepožadovaly konkrétní provozní prostředky nebo skupiny prostředků, ale aby byly požadavky na prostředky vyjádřeny pomocí charakteristik požadovaných prostředků. Plánovací modul potom bude moci přiřazovat vhodné provozní prostředky podle pracoviště, u kterého je výroba naplánována. Pokud například existují malé rozdíly v operačních časech nebo se přípravný čas některé operace liší podle pracoviště, můžete tyto informace určit přidáním dalšího vztahu operace k danému pracovišti.  

Chcete-li plně využít výhod sdílených postupů, používejte také spotřebu prostředků u odpovídajících kusovníků. Když na řádku kusovníku nastavíte příznak spotřeby prostředků, sklad a místo, odkud se mají vzít suroviny, se odvodí z provozního prostředku, u kterého je operace naplánována. Sklad a místo tedy není nutné určovat, dokud nebude výroba ve skutečnosti naplánována. Tímto způsobem můžete zajistit nezávislost kusovníku i postupu na fyzickém místě výroby produktu.

### <a name="standard-operation-relations"></a>Standardní vztahy operací

Pokud váš podnik používá při výrobě standardizované operace a parametry, jako je přípravný a operační čas, výpočty spotřeby či nákladů a podobně, se mění jen velmi málo nebo vůbec, můžete pro všechny operace vytvořit výchozí vztahy. V takovém případě nevytvářejte vztahy operací, které platí pro konkrétní postupy nebo uvolněné produkty.  

Pokud navíc vyjádříte požadavky na prostředky ve smyslu schopností a dovedností a vytvoříte postupy nezávislé na pracovištích, budete moci snížit množství práce spojené s údržbou podnikových procesů na minimum.  

Při použití tohoto přístupu budete operační časy a další vlastnosti sledovat a nastavovat především na stránce **Vztahy operací**.

### <a name="resource-specific-process-times"></a>Časy zpracování u konkrétních prostředků

Pokud v rámci požadavků na prostředky u operace nezadáte provozní prostředek nebo skupinu prostředků, mohou použitelné prostředky pracovat při různých rychlostech. Čas nutný ke zpracování operace se tedy může lišit. Tento problém můžete vyřešit tak, že způsob výpočtu času zpracování určíte pomocí pole **Vzorec** ve vztahu operace. Existují tyto možnosti:

-   **Standardní** – (výchozí možnost) výpočet použije pouze pole ze vztahu operace a vynásobí zadaný operační čas objednaným množstvím.
-   **Kapacita** – při výpočtu se bere v úvahu pole **Kapacita** u provozního prostředku. Čas tedy závisí na prostředku. Hodnota uvedená u provozního prostředku je kapacita za hodinu. Tato hodnota se vynásobí objednaným množstvím a hodnotou **Koeficient** ze vztahu operace.
-   **Dávka** – kapacita dávky se počítá s využitím informací ze vztahu operace. Počet dávek (a tím i čas zpracování) lze pak vypočítat na základě objednaného množství.
-   **Dávka prostředku** – tato možnost je v podstatě stejná jako možnost **Dávka**. Při výpočtu se však zohledňuje i pole **Kapacita dávky** z provozního prostředku. Čas tedy závisí na prostředku.


<a name="see-also"></a>Viz také
--------

[Kusovníky a receptury](bill-of-material-bom.md)

[Nákladové kategorie použité ve výrobních postupech](../cost-management/cost-categories-used-production-routings.md)

[Schopnosti prostředku](resource-capabilities.md)

[Přehled elektronických podpisů](/dynamics365/operations/organization-administration/electronic-signature-overview)




