---
title: Sestavy leasingu majetku
description: Toto téma uvádí a stručně popisuje sestavy, které jsou k dispozici pro leasing majetku.
author: moaamer
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 085027c5cc823beec99779791ff471dceb4ec8fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814097"
---
# <a name="asset-leasing-reports"></a>Sestavy leasingu majetku

[!include [banner](../includes/banner.md)]

Toto téma uvádí a stručně popisuje sestavy, které jsou k dispozici pro leasing majetku. Většina sestav se zobrazí po provedení těchto nebo velmi podobných kroků, jak je uvedeno). 

- Chcete-li zobrazit většinu sestav leasingu majetku, přejděte na **Leasing majetku > Dotazy a sestavy > Sestavy leasingu** a poté vyberte přehled, který chcete zobrazit. U sestav, které vyžadují jinou cestu výběru, jsou kroky k otevření sestavy zahrnuty do popisu této sestavy. 
- Když vyberete sestavu k tisku, otevře se stránka s parametry, která vám umožní filtrovat informace obsažené v sestavě. Zadejte kritéria filtru a poté volbou **OK** vygenerujete sestavu. Vygenerovaná sestava zobrazí informace, které spadají do filtrů, které jste zadali.

## <a name="asset-movement"></a>Přesun majetku
Sestava přesunutí majetku slouží jako souhrnná sestava o zůstatcích používaného majetku pro každý leasing. Tato sestava umožňuje zobrazit transakce majetku leasingu během zadaného období. Sestava obsahuje následující pole. 

|     Pole sestavy                  |     popis                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Datum zahájení              |     Datum zahájení nejstarší verze leasingu.                     |   
|     Doba trvání leasingu                     |     Doba trvání leasingu nejstarší verze leasingu.                            |
|     Krátkodobý leasing               |     Pokud je leasing klasifikován jako krátkodobý, zobrazí se **Ano**.         |
|     Leasing aktiv s nízkou hodnotou                |     Pokud je leasing klasifikován jako s nízkou hodnotou, zobrazí se **Ano**.          |
|     Počáteční používaný majetek     |     Původní hodnota používaného majetku z položky deníku počátečního uznání.      |
|     Počáteční zůstatek              |     Zůstatková účetní hodnota používaného majetku k datu v poli **Od data**.                         |
|     Odpisové výdaje období    |     Výše odpisových výdajů převzatá v časovém rozmezí definovaném pro sestavu.        |
|     Akumulovaný odpis       |     Výše kumulovaných odpisů k datu v poli **Od data**.                               |
|     Snížení hodnoty                     |     Částka, o kterou byla majetku snížena hodnota v časovém rozmezí definovaném pro sestavu.               |
|     Změny                  |     Částka úprav používaného majetku mezi parametry kalendářních dat.                            |
|     Zůstatková účetní hodnota                 |     Konečná zůstatková účetní hodnota používaného majetku, která je očištěná o kumulované odpisy k datu v poli **Do data**.    |

## <a name="differences-report"></a>Sestava rozdílů
Sestava Rozdíly ukazuje rozdíly mezi informacemi načtenými do rámce importu leasingu a informacemi, které jsou aktuálně v systému. To vám umožní porovnat, co bylo upraveno, aktualizováno nebo přidáno prostřednictvím rámce importu leasingu.  

Hodnoty v sestavě se budou lišit v závislosti na vybraném leasingu. Sestava zobrazí pouze ta pole, která se liší od toho, co je aktuálně v systému a co je v tabulkách fázování. Stará hodnota je to, co je aktuálně v systému nebo co bylo dříve v systému, v závislosti na tom, zda byl spuštěn proces importu. Nová hodnota ukazuje hodnotu, která je v tabulce fázování, která nahradí starou hodnotu.

## <a name="five-years-undiscounted-payment-forecast"></a>Pětiletá prognóza plných splátek
Sestava Pětiletá prognóza plných splátek zobrazuje předpokládané leasingové splátky v plné výši, které mají být zaplaceny během příštích pěti let od data uvedeného v parametrech sestavy. Sestava obsahuje následující pole. 

|     Pole sestavy         |     popis                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Popis leasingu     |     Popis leasingu v záhlaví leasingu.                                                      |
|     ID leasingu              |     Jedinečné ID leasingu.                                                                              |
|     Rezervovat                  |     Kniha leasingu přidružená k ID knihy.                                                         |
|     Klasifikace        |     Klasifikace leasingu.                                                                  |
|     Účtovací vrstva         |     Vrstva, ve které je zaúčtován tento leasing.                                                         |
|     Měna              |     Měna leasingu.                                                                        |
|     Aktuální               |     Součet všech leasingových splátek splatných během následujících 12 měsíců od data sestavy.          |
|     13–24 měsíců          |     Součet všech leasingových splátek splatných mezi 13 a 24 měsíci od data sestavy.           |
|     25–36 měsíců          |     Součet všech leasingových splátek splatných mezi 25 a 36 měsíci od data sestavy.           |
|     37–48 měsíců          |     Součet všech leasingových splátek splatných mezi 37 a 48 měsíci od data sestavy.           |
|     49–60 měsíců          |     Součet všech leasingových splátek splatných mezi 49 a 60 měsíci od data sestavy.           |
|     Poté            |     Součet všech leasingových splátek splatných za nebo po 61 měsících od data sestavy.              |

## <a name="gaap-cash-flows-report"></a>Sestava cashflow GAAP
Sestava zveřejnění údajů GAAP splňuje požadavek na zveřejnění údajů podle US GAAP uvedený v 842-20-50-4(g)(1). Chcete-li zobrazit tuto sestavu, přejděte na **Leasing majetku > Dotazy a sestavy > Zveřejněné údaje > GAAP – cashflow**. 

|     Pole sestavy                                 |     popis                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Od data <br> Do data                        |     Definuje rozsah kalendářních dat, který se používá k omezení informací obsažených v sestavě.      |
|     Právnická osoba                                  |     Právnická osoba vázaná na leasingy.                                      |
|     Typ leasingu                                    |     Klasifikace leasingu jako finančního nebo provozního.           |
|     ID leasingu                                      |     Jedinečné ID leasingu.                                                      |
|     Popis leasingu                             |     Popis leasingu v záhlaví leasingu.                              |
|     Kniha leasingu                                    |     Kniha leasingu, na kterou odkazuje řádek.                        |
|     Účtovací vrstva                                 |     Každá kniha, která je připojena k dlouhodobému majetku, se vytváří pro určitou účtovací vrstvu, která má celkový cíl odpisu.                          |
|     Skupina leasingu                                   |     Skupina, se kterou je svázán tento leasing.                                     |
|     Měna                                      |     Zkratka použité měny transakce. Všechny sestavy převedou měnu transakce na měnu vykazování.                      |
|     Finanční leasingy – operativní cashflow         |     Součet celkových zaúčtovaných variabilních splátek a celkových splátek úroků zaúčtovaných z amortizačního plánu mezi parametry kalendářních dat.        |
|     Finanční leasingy – finanční cashflow           |     Součet celkových plateb jistiny z amortizačního plánu mezi parametry kalendářních dat.       |
|     Operativní leasingy – operativní cashflow       |     Součet všech zaúčtovaných leasingových splátek a zaúčtovaných variabilních splátek mezi parametry data.            |

## <a name="lease-balances-forecast"></a>Prognóza zůstatků leasingu
Prognóza zůstatků leasingu uvádí informace přímo z plánu amortizace závazků a plánu odpisů majetku. Sestava zobrazuje prognózované částky předpokládaného leasingového závazku a používaného majetku za určité období, včetně všech předpokládaných výdajů pro tyto leasingy. Sestava obsahuje následující pole.

|     Pole sestavy                 |     popis                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Počáteční zůstatek             |     Počáteční zůstatek v amortizačním plánu leasingu pro období obsahující počáteční datum sestavy.            |
|     Počáteční uznání           |     Pokud datum zahájení leasingu spadá do časového období definovaného pro sestavu, zobrazí se v tomto sloupci hodnota účtu závazku položky deníku počátečního uznání.      |
|     Platby                      |     Součet splátek leasingu, které spadají do časového období definovaného pro sestavu.                               |
|     Zájmy                      |     Součet úrokových výdajů leasingu, které spadají do časového období definovaného pro sestavu.                    |
|     Konečný zůstatek                |     Zůstatek závazku leasingu k datu v poli **Do data**.                                                             |
|     Krátkodobý závazek          |     Částka krátkodobého závazku v amortizačním plánu leasingu k datu v poli **Do data**.                           |
|     Dlouhodobý závazek           |     Částka dlouhodobého závazku v amortizačním plánu leasingu k datu v poli **Do data**.                            |
|     Počáteční zůstatková účetní hodnota      |     „Počáteční zůstatková účetní hodnota“ v amortizačním plánu odpisu majetku leasingu pro období obsahující počáteční datum sestavy      |
|     Počáteční uznání           |     Pokud datum zahájení leasingu spadá do mezi parametry kalendářních dat sestavy, zobrazí se v tomto sloupci hodnota účtu majetku položky deníku počátečního uznání.            |
|     Odpisové výdaje          |     Součet výdajů na odpisy leasingu, které spadají do časového období definovaného pro sestavu.                  |
|     Konečný zůstatek                |     Zůstatek majetku leasingu k datu v poli **Do data**.                                                              |
|     Úprava jmění             |     Počáteční zůstatek minus počáteční zůstatková účetní hodnota.                                                             |

## <a name="lease-commencements-report"></a>Sestava zahájení leasingu
Sestava zahájení leasingu zobrazuje všechny leasingy, které byly zahájeny ve stanoveném časovém rozmezí, včetně počátečních závazků a zůstatků používaného majetku. Sestava obsahuje následující pole. 

|     Pole sestavy                 |     popis                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Datum zahájení             |     Datum položky deníku počátečního uznání, která byla zaúčtována pro tuto verzi leasingu.         |
|     Částka počátečních pasiv      |     Částka závazku z položky deníku počátečního uznání.                                  |
|     Částka počátečních aktiv          |     Částka majetku z položky deníku počátečního uznání.                                      |

## <a name="lease-modification-report"></a>Sestava změny leasingu
Sestava změny leasingu zobrazuje všechny leasingy, které byly změněny ve stanoveném časovém období. Sestava také ukazuje uživatele, který upravil leasing, a celkovou výši upraveného závazku. Sestava obsahuje následující pole. 

|     Pole sestavy                 |     popis           |
|---------------------------------  |-------------------------  |
|     Upravil/a                   |     Uživatelské jméno osoby, která změnila leasing.                                |
|     Datum úpravy               |     Datum, kdy byla zaúčtována položka deníku úpravy.                        |
|     Úpravy                   |     Částka za každou položku deníku úprav zaúčtovanou na účet závazku leasingu mezi parametry kalendářních dat. Kredity se objeví kladné, zatímco debety záporné.       |
|     Částka zisku (ztráty)            |     Částka za každou položku deníku úprav zaúčtovanou na účet zisku/ztráty leasingu mezi parametry kalendářních dat. Kredity se objeví kladné, zatímco debety záporné.       |
|     Pozdržené příjmy             |     Částka za každou položku deníku úprav zaúčtovanou na účet pozdržených příjmů leasingu mezi parametry kalendářních dat.      |
|     Konečný zůstatek pasiv      |     Výsledný zůstatek závazku k datu úpravy leasingu.           |

## <a name="lease-movement-report"></a>Sestava přesunutí leasingu
Sestava přesunutí leasingu slouží jako souhrnná sestava o zůstatcích závazku leasingu pro každý leasing. Tato sestava umožňuje uživateli zobrazit transakce závazku leasingu během zadaného období.

|     Pole sestavy             |     popis                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Datum zahájení         |     Datum zahájení nejstarší verze leasingu.    |
|     Doba trvání leasingu                |     Doba trvání leasingu nejstarší verze leasingu.           |
|     Zbývající splátky        |     Počet plateb, které ještě nebyly zaúčtovány pro leasing.                       |
|     Počáteční zůstatek         |     Součet všech transakcí ovlivňujících závazek leasingu, ke kterým došlo před počátečním datem sestavy.             |
|     Počáteční uznání       |     Částka jakékoli transakce počátečního uznání pro leasing, která byla zaúčtována v rozsahu dat definovaném pro sestavu.     |
|     Platby                  |     Součet platebních transakcí leasingu, které byly zaúčtovány v časovém období definovaném pro sestavu. Hodnoty v tomto sloupci se zobrazí jako záporné částky, protože platby snižují zůstatek závazku leasingu.  |
|     Zájmy                  |     Součet časových rozlišení úroků, které byly zaúčtovány pro leasing v časovém období definovaném pro sestavu.            |
|     Úpravy               |     Součet zaúčtovaných transakcí úprav leasingu, které spadají do časového období definovaného pro sestavu.                               |
|     Konečný zůstatek            |     Zůstatek všech transakcí závazku leasingu, které byly zaúčtovány k datu v poli **K datu** sestavy.                  |

## <a name="lease-transactions-report"></a>Sestava transakcí leasingu
Dotaz na leasingové transakce zobrazuje všechny položky deníku, které byly vygenerovány leasingem majetku. Každá položka deníku je přidružena k ID knihy, ze které pochází. To vám umožní snadno přidružit položku deníku k odpovídajícímu leasingu. Funkce dotazu na leasingové transakce funguje podobným způsobem jako stránka **Transakce dokladu** v hlavní knize.

## <a name="weighted-average-discount-rate-report"></a>Sestava sazby slevy váženého průměru
Sestava sazby slevy váženého průměru splňuje požadavek na zveřejnění dat US GAAP specifikovaný v ASC 842-20-50-4 (g) (4) pro sazbu slevy váženého průměru. Chcete-li zobrazit tuto sestavu, přejděte na **Leasing majetku > Dotazy a sestavy > Zveřejněné údaje > Sazba slevy váženého průměru**. Sestava obsahuje následující pole. 

|     Pole sestavy                     |     popis                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Od data                        |     Tato sestava bude zahrnovat všechny leasingy, které byly zahájeny k datu nebo před datem v poli **K datu**. Tato sestava by měla být spuštěna k poslednímu dni období, které má být zveřejněno.      |
|     Právnická osoba                      |     Právnická osoba, která je vázaná na leasing.                           |
|     ID leasingu                          |     Jedinečné ID leasingu.                                                  |
|     Popis leasingu                 |     Popis leasingu v záhlaví leasingu.                          |
|     Rezervovat                              |     Specifický typ knihy zobrazeného leasingu.                                                                                                                                            |
|     Účtovací vrstva                     |     Každá kniha, která je připojena k dlouhodobému majetku, se vytváří pro určitou účtovací vrstvu, která má celkový cíl odpisu.      |
|     Skupina leasingu                       |     Skupina, do které patří tento leasing.                                 |
|     Sazba slevy                     |     Sazba použitá jako sleva leasingových plateb.                             |
|     Měna                          |     Zkratka použité měny transakce. Všechny sestavy převedou měnu transakce na měnu vykazování.  |
|     Zbývající leasingové splátky          |     Celková částka nezaplacených leasingových splátek ze splátkového kalendáře zbývajících od data v poli **K datu**.            |
|     Zbývající vážené platby       |     Zbývající leasingové splátky vynásobené použitou sazbou slevy.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]