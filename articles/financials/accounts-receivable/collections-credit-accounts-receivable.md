---
title: "Úvěr a inkasa v modulu Pohledávky"
description: "Informace o inkasu pohledávek jsou spravovány v jednom ústředním zobrazení pomocí stránky Inkasa aplikace Microsoft Dynamics 365 for Finance and Operations. Vedoucí úvěrů a inkasa mohou používat toto centrální zobrazení ke správě inkas. Inkasní agenti mohou zahájit proces kolekce ze seznamů odběratelů, které jsou generovány pomocí použitím předem definované kolekce kritérií nebo stránky Odběratelé."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 23fc1a160cf25255a1677ca0e501c374746b6e34
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="credit-and-collections-in-accounts-receivable"></a>Úvěr a inkasa v modulu Pohledávky

[!INCLUDE [banner](../includes/banner.md)]

Informace o inkasu pohledávek jsou spravovány v jednom ústředním zobrazení pomocí stránky Inkasa aplikace Finance and Operations. Vedoucí úvěrů a inkasa mohou používat toto centrální zobrazení ke správě inkas. Inkasní agenti mohou zahájit proces kolekce ze seznamů odběratelů, které jsou generovány pomocí použitím předem definované kolekce kritérií nebo stránky Odběratelé.

Dříve než začnete s nastavením nebo práci s inkasem, měli byste se seznámit s následujícími koncepty:
-   Snímky pro sledování splatnosti odběratele obsahují informace o splatném zůstatku v určitém okamžiku
-   Fondy zákazníků kolekce pomáhají v uspořádání vaší práce
-   Inkasní agenti mohou mít své vlastní fondy zákazníků
-   Stránky seznamů umožňují uspořádat odběratele inkasa, aktivity a případy
-   Všechny informace o inkasu odběratele jsou na jedné stránku, která umožňuje provádět další akce
-   Odpuštění, obnovení nebo stornování úroků a poplatků je možné provést v jednom kroku
-   Vytvoření transakcí odpisů je možné provést v jednom kroku
-   Zpracování plateb s nedostatečnými finančními prostředky je možné provést v jednom kroku

Následující části popisují jednotlivé koncepty.

## <a name="customer-aging-snapshots"></a>Snímky sledování splatnosti odběratele 
Snímek sledování splatnosti obsahuje vypočtené splatné zůstatky pro odběratele v jednom bodu v čase. Tyto informace se zobrazí na stránce se seznamem Splatné zůstatky a Kolekce. Snímek sledování splatnosti musí být vytvořen dříve, než je možné zobrazit informace na stránkách se seznamem inkasa. 

Pro každého zákazníka obsahuje snímek sledování splatnosti záhlaví snímku sledování splatnosti a záznam podrobností, které odpovídají každému období pro sledování splatnosti v definici období pro sledování splatnosti. 

Záhlaví snímku sledování splatnosti obsahuje celkovou splatnou částku, limit úvěru, dodací list, částku, částku prodejní objednávky, počet sporných transakcí a celkovou částku sporných transakcí pro účet odběratele. Všechny transakce odběratele jsou zahrnuty do výpočtu těchto množství. Celková splatná částka, limit úvěru, částka dodacího listu a částka prodejní objednávky jsou zobrazeny v okně s fakty Informace o připsání na stranu Dal na stránce Inkasa. 

Pro každé období sledování splatnosti v definici období pro sledování splatnosti je vytvořen záznam podrobností pro snímek sledování splatnosti. Každý záznam podrobností o snímku pro sledování splatnosti obsahuje ID období sledování splatnosti a celkovou částku transakcí s daty, která jsou v období pro sledování splatnosti. Transakce jsou přidružené k období pro sledování splatnosti, jako je například 30 dnů po splatnosti. Datum se vztahuje ke sledování splatnosti k datu, které se stanoví během vytváření snímku sledování splatnosti. Tyto informace se zobrazí na stránce se seznamem Splatné zůstatky a v oknu s fakty Splatné zůstatky na stránce Kolekce.

## <a name="collections-customer-pools"></a> Fond zákazníků inkasa 
Fondy zákazníků představující dotazy, které definují skupinu odběratelských záznamů, které lze zobrazit a spravovat v rámci procesu inkasa nebo sledování splatnosti. Vyberte fondy zákazníků k filtrování informací pro stránku se seznamem Splatné zůstatky, Inkasní aktivity a Případy inkasa. Fondy zákazníků slouží také k filtrování účtů zákazníka, které budou zahrnuty při vytváření snímků pro sledování splatnosti.

## <a name="collections-agents"></a>Inkasní agenti
Standardně mohou uživatelé aplikace Microsoft Dynamics 365 for Finance and Operations zobrazit všechny informace o odběratelích na stránkách se seznamem inkasa. Můžete použít záznamy inkasního agenta a určit s nimi fondy zákazníků, kde je možné filtrovat informace na stránkách se seznamem inkasa a na stránce Inkasa. 

Inkasní agent je osoba, která pracuje s odběrateli k zajištění, že platby se vybírají včas. V aplikaci Finance and Operations jsou inkasní agenti pracovníci, kteří jsou přiřazeni uživatelům na stránce Nastavení uživatelů.

## <a name="collections-list-pages"></a> Stránky se seznamem inkasa 
Následující stránky se seznamem umožňují uspořádání informací o inkasu.
-   Splatné zůstatky – Sloupce na stránce seznamu obsahují zůstatky odběratelů a dlouhodobé částky podle období pro sledování splatnosti. Tyto informace jsou uloženy na snímku sledování splatnosti. Období pro sledování splatnosti je určeno podle použité definice období pro sledování splatnosti. Období pro sledování splatnosti je převzato z fondu zákazníků (pokud byl zadán v dotazu fondu). Pokud fond nemá definici období pro sledování splatnosti, použije se výchozí definice období pro sledování splatnosti určené na stránce Parametry pohledávek. Pokud není určena žádná výchozí definice období pro sledování splatnosti, je použita první definice období pro sledování splatnosti na stránce Období pro sledování splatnosti.
-   Inkasní aktivity – Sloupce na stránce seznamu obsahují aktivity, které jsou označeny jako inkasní aktivity. Tyto činnosti se vytvoří pomocí stránky Inkasa. Aktivity slouží ke sledování prováděné práce v souvislosti s inkasováním.
-   Případy inkasa – Sloupce na stránce seznamu obsahují informace o případech, které mají kategorii případu s typem případů Inkasa.

> [!NOTE]
> Snímek sledování splatnosti musí být vytvořen dříve, než je možné zobrazit informace na těchto stránkách se seznamem. Zobrazí se informace pouze pro odběratele, pro které byl vytvořen snímek sledování splatnosti. Záznamy, které se zobrazí na stránce seznamu, lze dále filtrovat následujícím způsobem:
> <li>Podle výchozího nastavení uživatel aplikace Finance and Operations má přístup ke všem zákazníkům, kteří mají snímek sledování splatnosti.</li>
> <li>Existují-li fondy zákazníků, uživatel musí být nastaven jako inkasní agent, aby mohl použít fondy pro filtrování informací na stránkách se seznamem inkasa. Informace jsou omezeny na odběratele, kteří jsou zahrnuti ve vybraném fondu odběratelů.</li>
> <li>Pokud je uživatel nastaven jako inkasní agent, pouze skupiny, které jsou vybrány pro daného inkasního agenta, jsou k dispozici na stránce se seznamem. Pokud vyberte možnost Povolit agentovi zobrazit všechny fondy zákazníků na stránce Inkasní agent pro inkasního agenta, všechny fondy budou k dispozici pro tohoto agenta.</li>


## <a name="collections-page"></a> Inkasní stránka
Na stránce Inkasa můžete sledovat, spravovat a reagovat na inkasní informace, aktivity a případy odběratele. 

Horní podokno obsahuje případy vybraného odběratele. Prostřední podokno zobrazí transakce odběratele. V dolním podokně se zobrazí aktivity odběratele. Můžete vytvořit případy inkasa a sledovat tak inkasní informace pro jednu nebo více transakcí a aktivit. Informace v horním a dolním podokně mohou být filtrovány podle případu. 

Okna s fakty zobrazí splatné zůstatky a kreditní limit pro vybraného odběratele. Tyto informace jsou uloženy na snímku sledování splatnosti. V případě potřeby můžete aktualizovat snímek sledování splatnosti s aktualizovanými informacemi. 

Podokno akcí obsahuje tlačítka, která zobrazují související informace pro vybraného odběratele, případ, transakci nebo aktivitu. Můžete provést také společné akce, jako například změnit inkasní stav transakce, odeslat e-mailovou korespondenci skrze integraci se svým poskytovatelem e-mailu, provést refundaci odběratelů, zpracovat platby NFP nebo odepsat neinkasovatelné zůstatky.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Možnost vzdát se, obnovit nebo změnit úrok nebo poplatky 
Můžete odpustit, obnovit nebo stornovat dokončená oznámení úroků nebo poplatky a úroky transakce, které jsou součástí oznámení úroků. To lze provést na kartě Inkaso v podokně akcí na stránce se seznamem všech odběratelů po klepnutí na oznámení úroků, úrok transakce nebo poplatek. 

Tyto úpravy mají vliv pouze na oznámeních úroků a úroky a poplatky, které tyto obsahují. Podle kroků v části "Vytvoření transakcí odpisů v jednom kroku“ vytvořte odpis všech poplatků, které zákazník dluží.

Další informace lze najít v části [Vytvoření kódu úroků s rozsahem](tasks/create-interest-code-range.md) a [Zpracování úroků](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Vytvoření transakcí odpisů
Můžete odepsat pochybné pohledávky klepnutím na možnost Odepsat ve formuláři Inkasa a na stránku se seznamem Splatné zůstatky, Odběratele a Otevřené odběratelské faktury. 

Při odepsání transakcí pro odběratele budou všechny transakce pro odběratele automaticky označeny k vyrovnání. Částka, která je odepsána, závisí na čisté částce označených transakcí. Transakce odpisu je vytvořena v obecném deníku a může obsahovat až tři typy řádků deníku.

-   První typ řádku deníku obsahuje položku pro odpis zákazníka. Pokud označené transakce obsahují více kombinací kódu měny, dimenze a účetní profily, bude vytvořen samostatný deník pro každou kombinaci.
-   Druhý typ řádku deníku obsahuje položku pro odpis hlavní knihy. Pokud označené transakce obsahují více kombinací kódu měny, dimenze a účetní profily, bude vytvořen samostatný deník pro každou kombinaci.
-   Třetí typ řádku deníku obsahuje informace o odpisu hlavní knihy pro DPH. Tento řádek deníku je vytvořen pouze, pokud je vybrána možnost Samostatná DPH na stránce Parametry pohledávek. Pokud označené transakce obsahují více kombinací účtu na vstupu DPH, dimenze a kódu DPH, bude vytvořen samostatný deník pro každou kombinaci.

Transakce odpisu je vytvořena v měně transakce.

Další informace lze najít v části [Vytvoření odpisového deníku pro zákazníka](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Zpracování plateb při nedostatečných finančních prostředcích (NFP)  
--------------------------------------------

Můžete zpracovat platby NFP klepnutím na možnost Platby NFP na stránce Inkasa. Klepnutím na toto tlačítko je platba zrušena. Pokud pro zákazníka platí nějaký poplatek NFP, v deníku plateb se vytvoří poplatek za transakci. Výše poplatku závisí na nastavení automatických nákladů. Automatické poplatky, které platí pro platby NFP jsou určeny podle skupiny nákladů, která je vybrána na stránce Bankovní účty pro související bankovní účet.






