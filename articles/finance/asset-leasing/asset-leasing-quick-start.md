---
title: Úvod k leasingu majetku
description: Tento článek popisuje schopnost leasingu majteku a prochází jednotlivými kroky pro vytvoření leasingu majetku a zobrazení informací o těchto leasinzích.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "4464"
- intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df4343031b3b116318f798f31adb4d1f6bed1db9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895131"
---
# <a name="asset-leasing-get-started"></a>Úvod k leasingu majetku

[!include [banner](../includes/banner.md)]

Tento článek popisuje schopnost leasingu majteku a prochází jednotlivými kroky pro vytvoření leasingu majetku a zobrazení informací o těchto leasinzích. Tento článek také definuje terminologii použitou v uživatelském rozhraní a dokumentaci. Leasing majetku je pokročilou schopností pro správu, sledování a automatizaci finančních transakcí pro pronajaté majetky (aktiva) v Microsoft Dynamics 365 Finance. Leasingu majetku vyhovuje mezinárodním účetním standardům (IFRS 16) a normám US GAAP (ASC 842). Leasing majetku zachycuje a zpracovává informace o leasinzích a pomáhá vygenerovat položky deníku v rámci celého životní cyklu leasingu od počátečního uznání, přes měsíční položky deníku, po snížení hodnoty a ukončení leasingu. Leasing majetku je možné bezproblémově integrovat s dalšími komponentami Dynamics 365 Finance, včetně Dlouhodobého majetku, Závazků a Hlavní knihy.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru **Správa funkcí** zkontrolovat stav funkce a zapnout ji, pokud je třeba. V pracovním prostoru **Správa funkcí** vyhledejte a vyberte funkci, která se jmenuje **Leasing majetku** a poté klikněte na tlačítko **Povolit nyní**.

Další informace o účetních standardech naleznete v tématu Standardní dokumentace pro IFRS 16 a US GAAP ASC 842.

## <a name="asset-leasing-elements"></a>Prvky leasingu majetku
Následující diagram ukazuje hlavní prvky obchodního procesu pro leasingy.

[![Prvky leasingu majetku.](./media/overview-01.png)](./media/overview-01.png)

Pronajatý majetek obsahuje následující hlavní součásti:

- **Leasingová smlouva** – Pronajímatel vlastní majetek a dohodne se s nájemcem na leasingu (pronájmu) majetku na konkrétní období výměnou za pravidelné leasingové platby. Kromě právní smlouvy mezi pronajímatelem a nájemcem zachycuje leasingová smlouva rozhodnutí o řízení, jako je pravděpodobnost uplatnění možnosti prodloužení a převod vlastnictví.

- **Výpočet a klasifikace leasingu podle účetního standardu** – Výpočet a klasifikace leasingu identifikují účetní standard, který bude použit při počátečním a následném měření, a také test klasifikace, který určuje, jakého typu leasingu bude. Leasing může být finanční leasing, operativní leasing, krátkodobý leasing nebo leasing majetku s nízkou hodnotou. Systém také vypočítává čistou současnou hodnotu budoucích minimálních leasingových splátek pro účely ocenění a klasifikace.

- **Leasingové transakce** – Leasing majetku podporuje počáteční uznání používaného majetku k leasingu v rozvaze, jakož i následné měření buď pro rozvahové leasingy, nebo mimorozvahové leasingy. Transakce počátečního uznání měří čistou současnou hodnotu budoucích minimálních leasingových splátek. Tato data se používají k určení hodnoty počátečního používaného majetku a leasingového závazku, které ovlivňují rozvahu organizace. Následné měření měsíčních leasingových transakcí zahrnuje kumulaci úroků z leasingového závazku, což zvyšuje leasingový závazek. Měří také narůstání leasingových splátek, které snižují leasingový závazek a které budou následně zaplaceny pronajímateli. Součástí měření je také amortizace používaného majetku.

  U mimorozvahových leasingů systém vypočítá lineární náklady na leasing, podle toho, která hodnota je nižší: ekonomická životnost majetku nebo doba trvání leasingu. Úpravy leasingu měří úpravy smlouvy, jako je prodloužení nebo rozšíření leasingu, a transakci snížení hodnoty, která využívá používaný majetek pro nevratné náklady.

  Leasing majetku se dá integrovat s hlavní knihou, aby se zajistilo, že všechny zaúčtované leasingové transakce aktualizují vaši účtovou osnovu. Leasing majetku se dá integrovat se závazky, aby bylo možné sledovat faktury pronajímatele v závazcích a odtud přijímat budoucí platby. Integrace s dlouhodobými majetky vám umožní sledovat leasingy v registru dlouhodobých majetků a účtovat transakce s používaným majetkem z dlouhodobých majetků, včetně počátečního uznání, odpisů a snížení hodnoty majetku.   

## <a name="asset-leasing-components"></a>Součásti leasingu majetku 
Leasing majetku mapuje informace o leasingu, platební kalendáře, data zahájení a ukončení a frekvenci splátek. Automatizuje také výpočty čisté současné hodnoty, měsíčních splátek leasingu, úroků a amortizace leasingu. Systém provádí klasifikační testy leasingu, a to v závislosti na konfiguraci. Systém také vytváří a zaúčtovává příslušné leasingové transakce, které jsou založeny na rámci definovaném v účetním standardu, který používáte.

Následující diagram ukazuje leasingovou knihu, leasing, vypočítaný platební kalendář, klasifikační testy leasingů a leasingových knih a odpovídající účetní transakce.

[![Leasing, leasingová kniha a platební kalendář.](./media/overview-02.png)](./media/overview-02.png)

- **Leasingová kniha** – Obsahuje všechny informace o leasingové smlouvě, jako jsou podmínky leasingu, reálná hodnota a leasingové splátky. Zahrnuje také účetní standard, který používáte, typ leasingu a prahové hodnoty, které jsou zohledněny v klasifikačním testu leasingu. Leasingová kniha také obsahuje leasingové transakce, které byly zaúčtovány do hlavní knihy. 
  
- **Leasing** – Leasing nese informace o leasingu majetku, které představují základ leasingu majetku, zdrojem informací o leasingu je leasingová smlouva a rozhodnutí o řízení, které se obě provádějí mimo Dynamics 365 Finance. Reálná hodnota majetku je cena, která by byla zaplacena za majetek v transakci k datu měření. Tato hodnota může záviset na typu majetku, tržních podmínkách a dalších kritériích, která lze při hodnocení zohlednit. Reálná hodnota majetku bude zohledněna v rovnici klasifikačního testu.

- **Očekávaná doba použitelnosti majetku** – Ta představuje zbývající období očekávané doby použitelnosti majetku od data zahájení leasingu. Očekávaná doba použitelnosti majetku bude zohledněna v rovnici klasifikačního testu. Liší se od očekávané doby použitelnosti definované v dlouhodobém majetku.

- **Přírůstková výpůjční úroková sazba** – Je to úroková sazba, která bude použita k výpočtu čisté současné hodnoty. K výpočtu čisté současné hodnoty leasingových splátek systém použije implicitní sazbu, pokud je definována v datech leasingu. Pokud implicitní sazba není definována, systém použije přírůstkovou výpůjční úrokovou sazbu.

- **Typ anuity** – Jde o leasingovou splátku splatnou buď na začátku platebního období, nebo na konci období. Může to být platba předem nebo splatná anuita (na začátku období splátky leasingu) nebo běžná anuita (na konci období splátky leasingu).

  První měsíc se bude považovat za období číslo nula pro platbu předem; první měsíc se bude považovat za období číslo jedna pro nedoplatek splátky.

- **Složený interval** – Ten představuje počet období, za které je úrok složen za rok. Může to být měsíčně (12 období ročně), čtvrtletně (4 období ročně), pololetně (2 období ročně) nebo ročně (1 období ročně). Počet období bude zohledněn při výpočtu čisté současné hodnoty.

- **Datum zahájení** – Je to datum, kdy pronajímatel zpřístupní majetek pro použití nájemcem. Všechny výpočty a transakce leasingu budou založeny na datu zahájení. Datum zahájení by mělo být na začátku období (prvního měsíce), aby byla zajištěna přesnost následných výpočtů. Můžete použít pole **Datum podpisu smlouvy** a zadat skutečné datum podpisu smlouvy.

- **Doba trvání leasingu** – Toto je délka doby leasingu v měsících.

> [!NOTE] 
> Definice doby trvání leasingu je založena na počtu období, neboli intervalů, v řádcích platebního kalendáře. Definovaný počet intervalů bude převeden na měsíce.

- **Řádek platebního kalendáře** – Zachycuje leasingové splátky za období. Rovněž specifikuje, zda bude uplatněno prodloužení a zahrnuto do počátečního měření používaného majetku a leasingového závazku. Můžete definovat počáteční datum leasingových splátek a intervaly období, které představují délku leasingu, což mohou být dny, měsíce nebo roky.

- **Četnost plateb** – Označuje, zda je platba měsíční, čtvrtletní, pololetní nebo roční. Koncové datum se počítá automaticky na základě počátečního data a počtu zadaných období.

- **Platební kalendář** – Jde o vypočtenou čistou současnou hodnotu založenou na době pokryté leasingovými splátkami, výši splátek, složeném období a typu anuity.

- **Období** – Jsou to období leasingu, která odrážejí složený interval a typ anuity. Složení interval určuje, jak budou období rozdělena. Můžete nastavit následující složené intervaly:

  - Měsíčně, 12 období ročně
  - Čtvrtletně, 4 období ročně
  - Pololetně, 2 období ročně
  - Ročně, 1 období ročně

První období začíná obdobím nula, pokud je typ anuity splatná anuita. Jinak první období začíná jedničkou, pokud je typ anuity nedoplatek splátky.

- **Měsíce** – Udává počet kalendářních měsíců po dobu trvání leasingu. Částka platby je splatná částka, jak je definována ve frekvenci plateb. Vypočítaná čistá současná hodnota je leasingová splátka založená na čisté současné hodnotě za období, složené intervaly a přírůstkovou výpůjční úrokovou sazbu.

> [!NOTE] 
> Čistá současná hodnota se počítá na základě rovnice diskontovaného peněžního toku.

- **Knihy** – Toto je předkonfigurované nastavení, které bude přidruženo ke každému leasingu. Kniha definuje použitý účetní standard, typy leasingu a prahovou hodnotu, která se používá jako základ pro klasifikační testy. Klasifikační testy se používají k automatickému určení typu leasingu.

- **Účetní soustava** – Ukazuje vybraný účetní standard, buď IFRS 16 a ASC 842, který podporujete. Účetní standard je určen v knize, která je přidružena k leasingu. Účetní standard určí účty hlavní knihy, které jsou uvedeny v profilu účtování.

- **Typy leasingu** – Označuje, který ze dvou typů leasingu bude použit, buď finanční leasing nebo operativní leasing. V rámci finančního leasingu jsou rizika a odměny související s pronajatým majetkem převedeny na nájemce. V rámci operativního leasingu rizika a odměny související s pronajatým majetkem zůstávají pronajímateli. Třetí možností je automatická identifikace typu leasingu, ať už finančního nebo operativního, na základě definovaných prahových hodnot v knize. Tato automatická identifikace se provádí během testu reklasifikace leasingu.

- **Prahové hodnoty** – Slouží v klasifikačních testech leasingu k určení, jestli je majetek klasifikován jako jedno z následujících:

  - **Doba trvání leasingu** – Toto je procento očekávané doby použitelnosti, které se má použít při klasifikačním testu. Systém klasifikuje leasing jako finanční, pokud je typ leasingu nastaven na automatický a je-li doba trvání leasingu na očekávanou dobu použitelnosti majetku větší než nebo rovna procentu zde definovanému.

  - **Čistá současná hodnota** – Toto je procento reálné hodnoty majetku, které se má použít při klasifikačním testu. Systém klasifikuje leasing jako finanční, pokud je typ leasingu nastaven na automatický a je-li čistá současná hodnota budoucích leasingových splátek na reálnou hodnotu majetku větší než nebo rovna procentu zde definovanému.

  - **Krátkodobý nájem** – Pokud je doba trvání leasingu menší než nebo rovna definované hodnotě, bude leasing klasifikován jako krátkodobý leasing.

  - **Nízká hodnota** – Pokud je reálná hodnota majetku menší než nebo rovna definované hodnotě, bude leasing klasifikován jako leasing aktiv (majetku) s nízkou hodnotou.

  - **Klasifikace a transakce leasingu** Klasifikace leasingu je automatizovaný proces klasifikace leasingů na základě definovaných prahových hodnot v knihách kromě dalších kritérií pro klasifikaci, aby se zjistilo, zda je leasing finanční leasing, operativní leasing, krátkodobý nájem (leasing) nebo leasing aktiv s nízkou hodnotou. To se také používá k identifikaci, zda je dodržen proces odložené splátky.

Klasifikační testy zahrnují převod vlastnictví, možnost nákupu, dobu trvání leasingu, čistou současnou hodnotu a unikátní majetek. Následující diagram ilustruje klasifikační testy leasingu.

[![Klasifikační testy leasingu.](./media/overview-03.png)](./media/overview-03.png)

Každý typ leasingu zpracovává účetnictví odlišně pro různé leasingové transakce. Transakce zahrnují počáteční uznání, úrokové náklady, splatnost leasingové splátky a odpisy leasingu a jsou založeny na účetních standardech, které používáte (IFRS 16 nebo ASC 842). Účty hlavní knihy jsou definovány v profilu účtování leasingu pro každý typ transakce a účetní rámec.

## <a name="asset-leasing-transactions"></a>Leasingové transakce s majetkem

#### <a name="initial-recognition"></a>Počáteční uznání 
Počáteční uznání pronajatého aktiva využívá vypočtenou čistou současnou hodnotu, aby ji bylo možné vykázat v rozvaze. Účetní položka pro toto je generována automaticky. Tato transakce odečte z účtu používaného majetku a připíše na účet závazku z operativního leasingu následujícím způsobem. Pokud je k leasingu přidružen dlouhodobý majetek, položka počátečního uznání se projeví jako pořízení dlouhodobého majetku. V této situaci musíte definovat profil účtování dlouhodobého majetku, abyste mohli účtovat na účet používaného majetku. 

> [!NOTE]
> Operativní leasing podporuje pouze US GAAP ASC 842.

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operativní leasing podle US GAAP            |     Používaný majetek        |     Závazek z operativního leasingu     |
|     Finanční leasing podle IFRS a US GAAP      |     Používaný majetek        |     Pasiva finančního leasingu       |

#### <a name="lease-liability-amortization-interest-expense"></a>Amortizace leasingového závazku (úrokové náklady) 
Úrok z leasingu se zjišťuje výpočtem úroku z počátečního zůstatku leasingu, leasingové splátky za období, úrokové výpůjční sazby a složených intervalových období za rok. Výše úroku zvyšuje účet závazku z operativního leasingu připsáním na něj, což se projeví v rozvaze organizace. Transakce rovněž zahrnuje debetní zápis na účet úrokových nákladů, který se odráží ve výkazu zisku a ztrát u finančního leasingu, a na účet nákladů na leasing u operativního leasingu.

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Položka závazku z operativního leasingu podle US GAAP ASC 842    |     Výdaje leasingu         |     Závazek z operativního leasingu         |
|     Položka závazku z finančního leasingu podle IFRS a US GAAP      |     Výdaje na úroky          |     Pasiva finančního leasingu           |

#### <a name="accrued-lease-payment"></a>Časově rozlišená leasingová splátka
Časově rozlišená leasingová splátka je uznána jako budoucí splátka leasingu, která má být zpracována jako platební transakce z bankovních nebo peněžních účtů. Splatná leasingová splátka snižuje leasingový závazek odečtením (debetováním) z účtu leasingového závazku oproti tomu, zda je dílčí hlavní kniha dodavatele v případě pronajímatele definována jako dodavatel, nebo zaúčtováním kreditní strany na účet hlavní knihy splatných směnek, poté bude platba provedena proti kterémukoli dodavateli nebo splatným směnkám.

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operativní leasing podle US GAAP              |  Závazek z operativního leasingu    |   Závazek dodavatele (dílčí hlavní kniha) / Splatné směnky  |
|     Finanční leasing podle IFRS a US GAAP        |  Pasiva finančního leasingu      |   Závazek dodavatele (dílčí hlavní kniha) / Splatné směnky  |

#### <a name="asset-depreciation"></a>Odpis majetku
Používaný majetek se odepisuje podle toho, co je menší – očekávaná doba použitelnosti majetku nebo doba trvání leasingu. Metoda výpočtu odpisů pro operativní leasing podle US GAAP (ASC 842) je založena na rozdílu mezi lineárním nákladem na leasing a částkou úroku. Odpisy u finančního leasingu se počítají standardní lineární metodou. Odpisy leasingu ovlivňují výkaz zisků a ztrát odečtením úrokových nákladů. Rozvaha je ovlivněna připsáním na naakumulovaný účet používaného majetku pro finanční leasing. Pokud je leasing spojen s dlouhodobým majetkem, odpisové transakce budou provedeny pouze z modulu dlouhodobého majetku. 

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operativní leasing podle US GAAP              |  Výdaje leasingu                |   Kumulované odpisy používaného majetku     |
|     Finanční leasing podle IFRS a US GAAP        |   Odpisy nákladů na používaný majetek   |   Kumulované odpisy používaného majetku    |

#### <a name="short-term-lease"></a>Krátkodobý leasing
Krátkodobý leasing je uznán jako náklad, který ovlivní výsledovku organizace. Vygenerovaná splatná leasingová splátka bude odečtena z účtu výdajů na leasing a připsána na účet splatných směnek nebo dílčí hlavní knihy dodavatele.

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Položka krátkodobého nájmu podle IFRS a US GAAP     |  Výdaje leasingu                |   Závazek dodavatele (dílčí hlavní kniha) / Splatné směnky  |

#### <a name="low-value-lease"></a>Leasing aktiv s nízkou hodnotou
Leasing aktiv s nízkou hodnotou je uznán jako náklad, který ovlivní výsledovku organizace. Vygenerovaná splatná leasingová splátka bude odečtena z výdajů na leasing a připsána ke splatným směnkám nebo dílčí hlavní knize dodavatele.

|     Typ                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Položka leasingu aktiv s nízkou hodnotou podle IFRS a US GAAP      |  Výdaje leasingu                |   Závazek dodavatele (dílčí hlavní kniha) / Splatné směnky  |


#### <a name="index-revaluation"></a>Přecenění indexu
Toto je účet leasingu majetku pro variabilní leasingové splátky měřený indexovou sazbou. Změny v leasingových splátkách způsobené kolísáním indexové sazby představují úpravu leasingu podle IFRS 16. Leasingový závazek a používaný majetek budou upraveny tak, aby zohledňovaly nové platby. 

|     Typ                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Položka přecenění indexu podle IFRS v případě zvýšení  |  Používaný majetek       |   Závazek z operativního leasingu |
|   Položka přecenění indexu podle IFRS v případě snížení  |  Závazek z operativního leasingu  |   Používaný majetek      |

Pokud se platby změní z důvodu změny indexové sazby, změní se pouze variabilní platby, jestliže nedojde k dalším změnám peněžních toků, například ke změně leasingových podmínek souvisejících s úrokovými sazbami podle US GAAP ASC 842.

#### <a name="lease-adjustment"></a>Úprava leasingu
Leasing majetku umožňuje upravit leasingy, pokud dojde ke změně podmínek leasingu, prodloužení leasingu nebo pokud existují další okolnosti, za kterých leasing vyžaduje úpravu. Úpravy leasingu jsou zaúčtovány za účelem zvýšení nebo snížení používaného majetku a leasingového závazku. Proces úpravy přebírá přenesené konečné zůstatky amortizace závazků a zůstatek majetku k datu úpravy. Když je leasing propojen s dlouhodobým majetkem, úprava používání bude zaúčtována pomocí ID, které je přiřazeno v dlouhodobém majetku. 

|     Typ                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Položka úpravy leasingu pro IFRS a US GAAP v případě zvýšení     |  Používaný majetek       |   Závazek z operativního leasingu |
|   Položka úpravy leasingu pro IFRS a US GAAP v případě snížení     |  Závazek z operativního leasingu  |   Používaný majetek      |


#### <a name="lease-impairment"></a>Snížení hodnoty leasingu
To představuje přenesení snížení zůstatku používaného majetku. Určete částku snížení hodnoty, datum transakce a zbývající období. Zbývající používaný majetek bude odepisován lineárně. Logika snížení hodnoty leasingu zohledňuje hodnotu přenesení majetku, která existuje v plánu odpisu majetku.  

|     Typ                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Položka snížení hodnoty pro IFRS a US GAAP           |  Výdaje snížení hodnoty                   |    Používaný majetek     |

>[!NOTE]
> Pokud je leasing spojen s dlouhodobým majetkem, mělo by se snížení hodnoty leasingu zaúčtovat z dlouhodobého majetku, protože odpisy majetku se spouští z modulu dlouhodobého majetku.

**Duální měna** Leasingové transakce lze účtovat v jiné měně, než je měna účetnictví a vykazování. Směnný kurz měny je definován v hlavní knize k datu zahájení. Směnné kurzy můžete změnit nastavením pole **Pevná sazba** na **Ano** při vytváření leasingu. Když zadáte leasingové transakce, počáteční uznání a následné odpisové transakce budou používat směnný kurz k datu zahájení. Při následných platebních a úrokových transakcích se použije aktuální aktivní směnný kurz. 

## <a name="create-an-asset-lease"></a>Vytvoření leasingu majetku
Pomocí následujících kroků vytvoříte nový leasing. 

1. Chcete-li používat **Leasing majetku**, musíte ho povolit v pracovním prostoru **Správa funkcí**. Z pracovního prostoru **Správa funkcí** vyberte **Vše**, aby se na stránce ukázaly všechny funkce. Vyberte **Leasing majetku** a poté vyberte **Povolit nyní**.
2. Přejděte na **Leasing majetku > Společné > Shrnutí leasingu**. Na pevné záložce **Obecné** zadejte povinná pole. 
   - **Podrobnosti leasingu**
   - **Očekávaná doba použitelnosti majetku (měsíce)**
   - **Skupina leasingu**
   - **Přírůstková výpůjční úroková sazba (%)**
   - **Interval úročení**
   - **Typ anuity**
   - **Měna**
   - **Datum zahájení**

3. Přejděte na pevnou záložku **Řádky platebního kalendáře** a zadejte platební řádek, poté vyberte **Vytvořit plány** (kalendáře).

4. Vyberte **Knihy**. 

5. Přepněte na pevnou záložku **Obecné**. Vypočítají se hodnoty **Počáteční používaný majetek** a **Leasingový závazek**. 

6. Přejděte na pevnou záložku **Klasifikační test leasingu** a zkontrolujte hodnotu v poli **Typ leasingu**. 

   Automatický **Typ leasingu** je klasifikován na základě kritérií, která jsou definována na stránce **Knihy**.

7.  Přejděte na **Platební kalendář** pod oddílem **Funkce**.  

   Stránka **Platební kalendář** uvádí budoucí platební kalendáře pro ID leasingu. Vyberte **Potvrdit kalendář**, abyste mohli zaúčtovávat transakce **Počáteční uznání**. 

[![Funkce Počáteční uznání.](./media/overview-13.png)](./media/overview-13.png)

8. Vyberte **Počáteční uznání** a vytvořte deník počátečního uznání. 

9. Vyberte **Deníky leasingu majetku** a zaúčtujte transakci počátečního uznání. 

   V platebním kalendáři můžete otevřít podrobnou stránku se seznamem transakcí používaného majetku. 
 
   **Plán amortizace leasingového závazku** zobrazuje částku úroku vypočítanou pro každé období.
   
10. Vytvořte deník a přejděte na **Deníky leasingu majetku**. **Plán amortizace leasingového závazku** se také zobrazuje v úrokových transakcích.

   Stránka **Plán odpisu majetku** zobrazuje odpisové transakce pro vybrané ID leasingu. 

   [![Stránka Transakce používaného majetku.](./media/overview-20.png)](./media/overview-20.png)

   Stránka **Transakce používaného majetku** uvádí počáteční uznání, akumulované odpisy a zůstatek majetku. 

   Stránka **Transakce leasingového závazku** zobrazuje počáteční uznání, splátky úroků z leasingu, splátky leasingu a zůstatek leasingového závazku. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
