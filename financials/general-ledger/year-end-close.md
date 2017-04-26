---
title: "Roční uzávěrka"
description: "Toto téma popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky zavřít hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Roční uzávěrka

[!include[banner](../includes/banner.md)]


Toto téma popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky zavřít hlavní knihy. 

Na konci fiskálního roku musíte spustit proces konce roku zavřít na převod počátečních zůstatků do nového roku. Většina organizací bude spuštěn proces konce roku zavřít několikrát. První bude získání zůstatků do nového fiskálního roku. Blízko konce roku lze poté spustit znovu, jako tolikrát, kolikrát je třeba, přesouvání zůstatky z nastavení položky do nového fiskálního roku. 

Během roku ukončit proces, existují dva typy možných transakce vytvořené. Počáteční transakce je vždy vygenerován a slouží k vytváření počátečních zůstatků v novém fiskálním roce. Počáteční transakce zobrazí salda účtů hlavní knihy rozvaha v novém fiskálním roce a zůstatků v novém fiskálním roce ze zůstatků na účtu hlavní knihy Zisk a ztráta v hlavní knihy účtu dosažených zisků. Uzávěrkové transakce je vytvořen volitelně uvést zůstatky účtů zisků a ztrát až nulovou uzavřením fiskálního roku.

## <a name="prepare-to-run-the-year-end-close"></a>Příprava ke spuštění konci roku zavřít
Před spuštěním procesu na konci roku zavřít, ověřte následující nastavení: 

Na stránce **Hlavní účet** proveďte toto:

-   Ověřit **typ účtu hlavní** je určeno pro každý hlavní účet. Typ hlavního účtu se používá k určení, zda zůstatek hlavním účtu bude uveden do vpřed jako počáteční zůstatek nebo uzavřené do nerozděleného zisku v počáteční transakce.
-   **Otevření účtu** pole lze použít k převodu zůstatek účtu hlavní nové hlavní účet během roku zavřít. Nový hlavní účet je zadána **otevření účtu** pole. Obvykle se používá pro rozvahové účty hlavní při hlavní účet je deaktivována a nový hlavní účet pro nový fiskální rok.

Na **parametry hlavní knihy** stránky v **uzavření fiskálního roku**:

-   **Odstranit uzavření transakcí roku** možnost se používá k určení, zda počáteční transakce generována z uzavření předchozího roku mají být odstraněny při dalším spuštění blízko konce roku. Pokud je tato možnost nastavena na **Ano**, je předchozí počáteční transakce odstraněny a nové počáteční transakce je založeno na aktuálních zůstatků. Pokud je tato možnost nastavena na **č**, zůstane předchozí počáteční transakce a další počáteční transakce je vytvořen přesunout zůstatky vpřed od úpravy transakce zaúčtované po ukončení předchozího roku.
-   **Vytvořit uzávěrkové transakce při převodu** možnost se používá k vytvoření transakcí uzávěrky fiskálního roku zavřít aby nulové zůstatky účtů zisků a ztrát. Pokud je tato možnost nastavena na **Ano**, je vytvořen počáteční transakce a uzávěrkové transakce. Pokud je tato možnost nastavena na **č**, je vytvořen pouze počáteční transakce do dalšího fiskálního roku k převodu zůstatků. Účet zisků a ztrát zůstatky zůstávají na konci fiskálního roku.
-   **Nastavit stav fiskálního roku trvale uzavřena** možnost slouží k nastavení fiskálního roku do stavu trvale uzavřeno. Pomocí tohoto nastavení opatrně, protože všechna období trvale uzavřené stavu nelze znovu otevřít, brání úpravy zaúčtování do fiskálního roku. Je nejvhodnější, nastavte **č**.
-   **Číslo dokladu musí být vyplněno** možnost se používá k definování, zda je číslo dokladu je požadována při spuštění procesu na konci roku zavřít. Je vhodné vyžadovat, aby bylo možné snadno identifikovat počáteční transakce číslo dokladu.

Na **fiskální kalendář** stránky:

-   Příští fiskální rok musí existovat před spuštěním ukončete na konci roku. Dalšího fiskálního roku je nutné k vytvoření počáteční zůstatky v otevřeném období.

V **kalendář hlavní knihy** stránky:

-   Volitelné: Jednotlivá fiskální období pro fiskální rok zavřený, může být nastavena na **na blokování** Chcete-li zabránit nové transakce se. Upravte položky jsou, při zjištění blokování období dále lze opět otevřít zaúčtujte položky úprav i v případě, že již byl spuštěn proces konce roku zavřít.

## <a name="define-year-end-close-templates"></a>Definovat šablony roční zavřít
Po konfiguraci systému můžete spustit proces konce roku zavřít. Na **uzávěrka** stránce šablony mohou být definovány pro skupinu právnických osob, jejichž uzávěrka proces spustí. Šablona bude znovu použít na každého roku zavřít, ale lze změnit, pokud změny v organizaci. 

Nejprve definovat **název skupiny** pro šablonu a vyberte fiskální kalendář. Název skupiny by měl identifikovat skupiny právnických osob, které jsou zahrnuty.  Například šablony může nastavena na základě zeměpis, se zvláštní skupiny vytvořené pro Severní Ameriky právnické osoby, právnické osoby EMEA a APAC právnické osoby. 

Právnické osoby dále lze přidat do šablony. Právnické osoby lze přidat výběrem organizační hierarchie nebo výběrem právnické osoby. Pokud je vybrána organizační hierarchie, pouze právnických osob v rámci hierarchie používající vybraného fiskálního kalendáře bude přidán do šablony. Přidat do šablony pomocí právnické osoby, mohou být přidány pouze právnické osoby se stejný fiskální kalendář. Stejný fiskální kalendář je vyžadován, protože je blízko konce roku spustit výběrem fiskálního roku, které se může lišit od kalendáře kalendář. 

Po přidání právnických osob se definujte nerozděleného zisku hlavní účty pro každou právnickou osobu. **Loni koncové datum uzavření** pole bude aktualizováno při každém spuštění zavřít konec roku pro právnickou osobu. 

**Finanční dimenze** karta slouží k definování finanční dimenze, které budou používány na počáteční transakce. Definování nastavení se týkají pouze právnické osoby, které jsou vybrány v **právnické osoby** mřížky. Instalační program bude opakovat pro každou právnickou osobu v mřížce. 

**Transfer rozvahy rozměry** slouží k definování, zda finanční dimenze transakcí zaúčtovaných na účty rozvahy se uchovávají na počáteční transakce. Je vhodné nastavit tuto možnost na **Ano**. **Převod zisků a ztrát rozměry** slouží k definování, které finanční dimenze pro transakce zaúčtované k zisku a ztrát bude převedena do hlavního účtu dosažených zisků. Nejprve určete finanční dimenze, které jsou relevantní pro vybrané právnické osoby. To by zahrnovalo všechny finanční dimenze účtováno v roce i v případě, že finanční dimenze není součástí aktivní účetní struktuře. Dále určete každou dimenzi jako **zavřít jeden** nebo **zavřít všechny**.  Výchozí hodnota je **zavřít všechny**, která udržuje původní finanční dimenze hodnoty ze zaúčtovaných transakcí a používá je pro vytvoření otevření zůstatky účtu dosažených zisků. Vytvoří se samostatné nerozděleného zisku počáteční zůstatky pro každou jedinečnou kombinaci hodnot finančních dimenzí. Pokud **zavřít jeden** je vybrána, všechny transakce zaúčtované s finanční dimenze budou shrnuty do nerozděleného zisku počáteční saldo pro hodnotu dimenze zadané v poli po **zavřít jeden**. Předpokládejme například, že se strukturou účtu hlavní účet – oddělení byly zaúčtovány všechny transakce pro fiskální rok. Pro finanční dimenzi oddělení v šabloně **zavřít jeden** zaškrtnuto a zadaná hodnota je 100. Pokud jde o celkový výnos všechny transakce zaúčtované do oddělení 200, 300 a 400 $100,000, bude vytvořen jeden počáteční zůstatek pro Retained zisky - 100. Vyberete-li **zavřít jeden** a ponechejte prázdné hodnoty finanční dimenze, všechny transakce zaúčtuje nerozděleného zisku s touto hodnotou dimenze jsou prázdné. 

Účetní struktury neodpovídající zavřít procesu na konci roku. Důvodem je skutečnost, že účetní struktury můžete změnit celý fiskální rok a není vždy možné identifikovat příslušné účetní struktury z důvodu těchto změn.  Při vytváření počátečních transakcí salda bude třeba posunout dopředu s finanční dimenze definované v šabloně zavřít konec roku. Počáteční zůstatky položky mohou zahrnovat finanční dimenze již v aktuální účet strukturu a segment kombinace, které již nejsou platné ve struktuře účtu aktuální. Pokud vaše organizace chce vyloučit finanční dimenze dosažených získávat počáteční zůstatek, nastavit finanční dimenze **zavřít jeden** a ponechat prázdnou hodnotu dimenze.

## <a name="run-the-year-end-close-process"></a>Spustit proces konce roku zavřít
Po vytvoření šablony roční uzavření roku Zavřít proces je zahájen výběrem **fiskálního roku spusťte** v podokně akcí. Vyberte všechny nebo část právnické osoby ze šablony, pro který chcete spustit konci roku zavřít. Při spuštění konci roku uzavřít poprvé ve fiskálním roce, bude pravděpodobně zvolíte všechny právnické osoby, chcete-li vytvořit počáteční zůstatky pro všechny právnické osoby. Pokud pracujete konci roku Zavřít znovu, můžete spustit proces pouze právnické osoby, pro které byly úpravy položky zaúčtovány. 

Vyberte fiskální rok, který chcete zavřít proces konce roku proti spuštění. Pokud existuje více než jeden zavírací dobu pro poslední období fiskálního roku **název období** pole bude k dispozici, takže můžete vybrat které období uzávěrky Zaúčtovat uzávěrkové transakce-li instalační program vytvořit uzávěrkové transakce. 

Dokladu zadejte číslo, které nebo nemusí být vyžadovány v závislosti na nastavení obecné parametry hlavní knihy. Stejné číslo dokladu se použije pro všechny právnické osoby vybrané pro uzavření proces konce roku. Číslo dokladu není generována pomocí číselné řady. Je vhodné zadat číslo dokladu, i když není vyžadováno. Zadejte číslo dokladu je snazší najít počátečních transakcí do nového fiskálního roku. Pokud není zadáno číslo dokladu, dokladu bude prázdné pro počáteční transakce. 

Pokud chcete stornovat konci předchozího roku zavřít pro vybraný fiskální rok, nastavte **vrátit zpět předchozí blízko** k **Ano**. Blízko konce roku bude stornována, ale proces můžete kdykoli znovu spustit. Pokud zpětné zavřete, konci roku **Loni koncové datum uzavření** není k dispozici. 

Výchozí proces konce roku zavřít spustit v dávkovém režimu. Je osvědčeným postupem spuštění procesu v dávkovém režimu, umožňující uživateli návrat na jiné činnosti. Po dokončení zavřít proces konce roku **Loni koncové datum uzavření** bude aktualizováno datum relace.

Další informace naleznete v tématu [zavřít na konci období hlavní knihy](close-general-ledger-at-period-end.md).




