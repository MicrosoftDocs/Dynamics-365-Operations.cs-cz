---
title: Nevyfakturované výnosy
description: Toto téma vysvětluje, jak nastavit položky a účty pro použití funkce nevyfakturovaných výnosů ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4a5bd016649957d90876d4eb50c358cd9d6fba80
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629398"
---
# <a name="unbilled-revenue"></a>Nevyfakturované výnosy

Toto téma popisuje funkci nevyfakturovaných příjmů, která umožňuje zahrnout částky za celé rozvrhy fakturace do rozvahy. Tyto částky jsou zahrnuty na účtu nevyfakturovaných výnosů a na účtu kompenzace nevyfakturovaných výnosů a smlouva je fakturována prostřednictvím splátek.

## <a name="set-up-unbilled-revenue"></a>Nastavení nevyfakturovaných výnosů

Chcete-li nastavit nefakturovaný výnos, postupujte následujícím způsobem.

- na stránce **Parametry opakované fakturace smlouvy** nastavte pole v části **Nefakturované výnosy**.
- Funkci nevyfakturovaných výnosů lze použít pro položky, u kterých je pole **Typ položky** nastaveno na **Standardní**. Lze jej použít i na odložené položky. Chcete-li použít nevyfakturované výnosy s krátkodobou funkcí, nastavte krátkodobé možnosti na stránce **Parametry opakované fakturace smlouvy**.

Chcete-li nastavit položky pro použití nefakturovaného výnosu, postupujte následujícím způsobem.

1. Na stránce **Nastavení nefakturovaných výnosů** na kartě **Položky** vyberte **Přidat**.
2. Na novém řádku v okně **Kód položky** vyberte kód položky.
3. V poli **Vztah položky** vyberte vztah položky.
4. Zopakujte tyto kroky, chcete-li přidat další řádky.
5. Zvolte možnost **Uložit**.

Chcete-li nastavit položky a účty nevyfakturovaných výnosů, postupujte podle následujících kroků.

1. Na stránce **Nastavení nefakturovaných výnosů** na kartě **Účty** vyberte **Přidat**.
2. Na novém řádku v okně **Kód položky** vyberte kód položky.
3. V poli **Vztah položky** vyberte vztah položky.
4. Vyberte účty pro nevyfakturované výnosy, nevyfakturovanou slevu a vyrovnání nevyfakturovaných výnosů. Chcete-li používat krátkodobé účty, musíte nastavit hodnotu v poli **Krátkodobá nefakturovaná metoda** na **Období prosazení** nebo **Pevný rok** na stránce **Parametry opakované fakturace smlouvy**.
5. Zopakujte tyto kroky, chcete-li přidat další řádky.
6. Zvolte možnost **Uložit**.

## <a name="use-unbilled-revenue"></a>Použití nevyfakturovaných výnosů

1. Na stránce **Všechny plány fakturace** vytvořte plány fakturace.
2. Pokud položka ještě není nastavena pro použití nevyfakturovaných příjmů, zaškrtněte políčko **Nevyfakturované příjmy** na řádku plánu fakturace.
3. Nastavte hodnotu možnosti **Nefakturovaný výnos** na **Ano**. Poté zkontrolujte a podle potřeby upravte účty nevyfakturovaných výnosů, slev a zápočtů nevyfakturovaných výnosů.
4. Na rozpisu účtování v části **Zpracování nevyfakturovaných výnosů** vyberte **Vytvořte položku deníku** k vytvoření počátečního zápisu do deníku pro nevyfakturované výnosy. Tento krok je nutné provést před fakturací plánu účtování.
5. Po vytvoření počáteční položky deníku vyberte **Vygenerovat fakturu** k vytvoření prodejních objednávek a zaúčtování faktur pro fakturační plány.
6. Po zaúčtování faktur si můžete prohlédnout informace o auditu na kartě **Obnovení** na stránce **Všechny plány fakturace**.

### <a name="milestone-billing"></a>Vyúčtování po milnících

Vyúčtování po milnících funguje s nevyfakturovanými výnosy za následujících podmínek:

- Pokud je nadřazená položka milníku nefakturována (je zaškrtnuto políčko **Nefakturované výnosy**) a budou účtovány podřízené položky milníku (zaškrtávací políčko **Nevyfakturované příjmy** je prázdné), musí být specifikováno počáteční a koncové datum nadřazené položky. Tato data se používají k vytvoření počáteční položky deníku.
- Pokud je nadřazená položka milníku nefakturována (políčko **Nefakturované výnosy** je prázdné) a budou účtovány podřízené položky milníku (zaškrtávací políčko **Nevyfakturované příjmy** je zaškrtnuto), datum ukončení musí být zadáno pouze pro podřízené položky, pro které chcete vytvořit počáteční záznam do deníku.

Každou podřízenou položku milníku lze zpracovat samostatně. Koncová data lze zadat, když jste připraveni vytvořit počáteční položku deníku.

> [!NOTE]
> Pokud již byla vytvořena počáteční položka deníku pro nadřazenou položku milníku nebo podřízené položky nebo byla vytvořena faktura, nelze počáteční a koncové datum upravit.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Nevyfakturované výnosy s rovnoměrným časovým rozlišením

Chcete-li použít nevyfakturované výnosy s rovnoměrným časovým rozlišením, postupujte podle následujících kroků.

1. Na stránce **Všechny plány fakturace** vytvořte plány fakturace.
2. Přidejte položku do řádků plánu vyúčtování.
3. Pro řádek vyberte **Odpisy**.
4. Na stránce **Odložení transakce** postupujte takto:

    1. Nastavte možnost **Odložené** na **Ano**.
    2. Změňte účty podle potřeby.
    3. V části **Plán** vyberte **Přímka** a podle potřeby upravte další hodnoty.
    4. Vyberte **OK**.

5. Vyberte pole **Nefakturovaný výnos** pro řádek a poté postupujte takto:

    1. Nastavte hodnotu možnosti **Nefakturovaný výnos** na **Ano**.
    2. Vyberte účty pro použití u výnosu, nevyfakturovanou slevu a vyrovnání nevyfakturovaných výnosů.

6. V plánu fakturace vyberte v části **Zpracování nevyfakturovaných příjmů** možnost **Vytvořit položku deníku**. Případně použijte stránku **Hromadné zpracování nevyfakturovaných výnosů** k vytvoření položky deníku.
7. Vytvoří se plán odložení. Na stránce **Všechny plány odkladů** si můžete prohlédnout podrobnosti. Po vytvoření plánu odkladů můžete upravit různé hodnoty pro položku plánu vyúčtování. Můžete například upravit jednotkovou cenu, množství nebo data.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Nevyfakturované tržby s odklady na základě událostí

Chcete-li použít nevyfakturované příjmy s rozvrhem odkladu na základě události, postupujte podle následujících kroků.

1. Na stránce **Všechny plány fakturace** vytvořte plány fakturace.
2. Přidejte položku do řádků plánu vyúčtování.
3. Pro řádek vyberte **Odpisy**.
4. Na stránce **Odložení transakce** postupujte takto:

    1. Nastavte možnost **Odložené** na **Ano**.
    2. Změňte účty podle potřeby.
    3. V části **Plán** vyberte **Na základě události**, **Šablona**, **Typ přidělení** a **účet vypršení platnosti**.
    4. Vyberte **OK**.

5. Vyberte pole **Nefakturovaný výnos** pro řádek a poté postupujte takto:

    - Nastavte hodnotu možnosti **Nefakturovaný výnos** na **Ano**.
    - Vyberte účty pro použití u výnosu, nevyfakturovanou slevu a vyrovnání nevyfakturovaných výnosů.

6. V plánu fakturace vyberte v části **Zpracování nevyfakturovaných příjmů** možnost **Vytvořit položku deníku**. Případně použijte stránku **Hromadné zpracování nevyfakturovaných výnosů** k vytvoření položky deníku.
7. Vytvoří se plán odložení. Na stránce **Všechny plány odkladů** si můžete prohlédnout podrobnosti. Po vytvoření plánu odkladů můžete upravit různé hodnoty pro položku plánu vyúčtování. Můžete například upravit jednotkovou cenu, množství nebo data. Plán odkladu je přepočítán na základě nových hodnot.

Distribuce jsou přepočítány na základě zvoleného typu přidělení (**Procento**, **Procento dokončení** nebo **Stejné částky**). Pro typ přidělení **Variabilní částky** se distribuce přepočítá na základě procentuálního ekvivalentu počáteční hodnoty pro událost. Například původní jednotková cena je 100,00 USD a procento počáteční hodnoty je 55,00 USD (55 procent). Pokud se jednotková cena změní na 200,00 USD, variabilní částka události se stane 110,00 USD (stále 55 procent).

> [!NOTE]
> Pokud byly rozpoznány řádky plánu odkladu, nelze řádkovou položku plánu fakturace upravit. Chcete-li upravit řádkovou položku, musíte nejprve obrátit rozpoznané řádky. Řádek plánu fakturace lze poté aktualizovat.

### <a name="unbilled-revenue-and-top-billing"></a>Nevyfakturované tržby a nejvyšší fakturace

Plán účtování je zadán na tři roky a faktury jsou účtovány ročně po dobu tří let. Celá částka smlouvy je zaznamenána na účtu nevyfakturovaných výnosů, ze kterého jsou vytvářeny roční faktury. Offsetový účet je výnos nebo účet výnosů příštích období.

Všimněte si, že nejvyšší fakturace a nevyfakturované příjmy nefungují společně, protože v hlavní knize mohou nastat problémy s odsouhlasením. Například na stránce **Nastavení skupiny položek** je skupina položek A nastavena tak, že je pole **Počet horních řádků** nastaveno na **2**. Na stránce **Plány fakturace** jsou přidány tři položky. Všechny tři položky patří do skupiny položek A. Při vytváření prvotního zápisu do deníku pro funkci nevyfakturované výnosy se částka za všechny tři položky zpracuje na nevyfakturovaný účet. Při vytváření faktury pro plán vyúčtování jsou zahrnuty pouze částky za dvě nejvyšší položky. Proto částka faktury neodpovídá částce, která byla zpracována na účet nevyfakturovaných výnosů, a v hlavní knize vznikají problémy s odsouhlasením.

Pokud chcete použít nevyfakturované výnosy, ponechte stránku **Nastavení skupiny položek** prázdnou nebo nastavte všechny skupiny položek tak, aby bylo pole **Počet horních řádků** nastaveno na **0** (nula). Pokud chcete použít nejvyšší fakturaci, nejsou k dispozici žádné akce s nevyfakturovanými příjmy.

### <a name="examples"></a>Příklad

Od verze 10.0.27 je při použití nevyfakturovaných výnosů zaveden nový účet. Když je zaúčtován počáteční proces **Vytvořit deníkovou položku**, kredit se provede na nový nevyfakturovaný účet pro vyrovnání výnosů. Tento účet se používá místo účtu výnosů, protože stejná hodnota musí být stornována při fakturaci podle účtového rozvrhu. Pokud se vyskytnou kurzové nebo zaokrouhlovací rozdíly, částky, které se počítají v průběhu procesu **Vygenerovat fakturu**, může být proces jiný. Toto chování zajišťuje, že čistá částka účtů je 0 (nula).

Tento příklad ukazuje, jak použít nevyfakturované výnosy k vykázání celé částky smlouvy v rozvaze jako nevyfakturovaných výnosů. Druhá strana záznamu je kompenzace nevyfakturovaných výnosů. Když fakturujete zákazníkovi, nevyfakturované výnosy a kompenzace nevyfakturovaných výnosů se stornují. K uznání výnosů dojde buď v době fakturace, nebo podle nastaveného rozvrhu účtování s odložením.

#### <a name="assumptions"></a>Předpoklady

- Zákazník podepíše 1. ledna běžného roku smlouvu na tři roky za 390 USD.
- Smlouva obsahuje dvě části: licence a smlouvu o údržbě.
- Prodejní cena licenčního poplatku je 300 USD a zákazníkovi bude 1. ledna každého smluvního roku fakturováno 100 USD. Licenční poplatek ve výši 300 USD bude při podpisu smlouvy považován za příjem.
- Prodejní cena poplatku za údržbu je 90 USD a zákazníkovi bude 1. ledna každého smluvního roku fakturováno 30 USD. Poplatek za údržbu ve výši 90 USD bude odložen a 2,50 USD bude uznáno každý měsíc po dobu trvání smlouvy.
- Na začátku každého ze tří let trvání smlouvy (1. ledna) bude zákazníkovi vystavena faktura na 130 USD.

#### <a name="steps"></a>Kroky

1. Nastavte dvě uvolněné položky jako nevyfakturované položky. Použijte **Nastavení nevyfakturovaných příjmů** k nastavení položek a účtů, které používají nevyfakturované příjmy.
2. V tomto příkladu je poplatek za údržbu odložen. Položka vyžaduje šablonu odložení, která je nastavena na stránce **Šablony odkladu**. Šablona má frekvenci období **Měsíční** a délka období uznání 36 měsíců. Výnos za měsíc tedy činí 2,50 USD.
3. Na stránce **Položky jsou ve výchozím nastavení odložené** nastavte hodnotu v poli **Udržovací poplatek** na **Odložitelná položka**. Tento a další krok způsobí, že položka poplatku za údržbu bude odložena, když je prodána nebo zahrnuta do plánu fakturace.
4. Vyberte **Výchozí hodnoty odkladu** \> **Šablona** a přidejte položku pro poplatek za údržbu a rovnou šablonu z kroku 2. Položka udržovacího poplatku bude spojena s 36měsíčním plánem odkladu.
5. Vytvořte plán fakturace, který bude zahrnovat dvě nefakturované položky. Plán fakturace pro smlouvu je nastaven s následujícími položkami.

    | Položka | Počáteční datum | Datum ukončení | Částka | Frekvence fakturace | Odložená položka | Nevyfakturované výnosy | Popis |
    |---|---|---|---|---|---|---|---|
    | Licence | 1. ledna, CY | 31. prosince CY+2 | $100.00 | Ročně | Číslo | Ano | Zákazníkovi bude každý rok fakturováno 100,00 USD. Celková částka 300,00 USD bude předem zaznamenána jako nevyfakturované výnosy v rozvaze a jako výnosy do zisku a ztráty. Každá faktura sníží nevyfakturovanou částku. |
    | Údržba | 1. ledna, CY | 31. prosince CY+2 | $30,00 | Ročně | Ano | Ano | Zákazníkovi bude každý rok fakturováno 30,00 USD. Celková částka 90,00 USD bude předem zaznamenána jako odložený výnos v rozvaze. Každá faktura sníží nevyfakturovanou částku. Výnosy příštích období budou účtovány měsíčně po dobu 36 měsíců. |

6. Na stránce **Všechny plány fakturace** použijte proces **Vytvořit deníkovou položku** k zaúčtování hodnoty smlouvy do rozvahy jako nevyfakturovaný výnos.

Jsou vytvořeny dvě deníkové položky, jedna pro každý řádek fakturačního plánu.

| Účet nevyfakturovaných výnosů | Protiúčet nevyfakturovaných výnosů | Částka Má dáti | Částka Dal |
|---|---|---|---|
| Účet nevyfakturovaných výnosů | | $300.00 | |
| | Protiúčet nevyfakturovaných výnosů | | $300.00 |

| Účet nevyfakturovaných výnosů | Odložené výnosy | Částka Má dáti | Částka Dal |
|---|---|---|---|
| Účet nevyfakturovaných výnosů | | $90.00 | |
| |Odložené výnosy údržby | | $90.00 |

První položka deníku se zaúčtuje na účet vyrovnání nevyfakturovaných výnosů a druhý se zaúčtuje na účet výnosů příštích období. Pokud má řádek fakturace jak nevyfakturované výnosy, tak výnosy příštích období, použije se účet výnosů příštích období, nikoli vyrovnání nevyfakturovaných výnosů. Smlouva vyžaduje, aby faktura pro zákazníka byla vytvořena na začátku každého roku. Použijte proces **Vygenerovat fakturu** k vytvoření faktury. Po vytvoření faktury se vytvoří následující položky deníku.

| Hlavní účet | Účet nevyfakturovaných výnosů | Částka Má dáti | Částka Dal |
|---|---|---|---|
| Protiúčet nevyfakturovaných výnosů | | $100.00 | |
| | Účet nevyfakturovaných výnosů | | $100.00 |
| Pohledávky | | $100.00 | |
| | Výnosový účet | | $100.00 |

| Hlavní účet | Účet nevyfakturovaných výnosů | Částka Má dáti | Částka Dal |
|---|---|---|---|
| Účet odložených výnosů z údržby | | $30,00 | |
| | Účet nevyfakturovaných výnosů | | $30,00 |
| Pohledávky | | $30,00 | |
| | Účet odložených výnosů z údržby | | $30,00 |

Stejná položka deníku bude vytvořena fakturami, které budou zaúčtovány na začátku příštích dvou let. Čistá částka účtu výnosů příštích období bude 0 (nula), protože nedochází k žádným rozdílům způsobeným zaokrouhlením ani kurzovým rozdílům. Výnosy příštích období musí být stornovány přesně tak, jak byly připsány v průběhu procesu **Vytvořte zápis do deníku**. Protože výnosy jsou stále odložené a budou zaúčtovány později, dojde znovu k připsání na účet odložených výnosů.

V posledním kroku se každý měsíc vytvoří zápis do deníku pro uznání výnosů z odložených poplatků za údržbu. Položku deníku lze vytvořit pomocí stránky **Zpracování rozpoznávání**. Případně jej lze vytvořit výběrem možnosti **Uznání** pro řádky na stránce **Plán odkladu**.

| Účet odložených výnosů | Výnosový účet | Částka Má dáti | Částka Dal |
|---|---|---|---|
| Odložené výnosy údržby | | $2.50 | |
| | Požadavek na údržbu | | $2.50 |

Tato položka deníku se vytvoří pokaždé, když se pro tuto odloženou položku spustí proces rozpoznávání (celkem 36krát).

#### <a name="short-term-fixed-year"></a>Krátkodobé: pevný rok

Chcete-li použít nevyfakturované výnosy s krátkodobou funkcí, nastavte hodnotu v poli **krátkodobé nefakturované** na stránce **Parametry opakované fakturace smlouvy**. Následující příklad ukazuje výpočty, které se provádějí při použití nevyfakturovaných výnosů spolu s metodou **Pevný rok** pro krátkodobé nevyfakturované výnosy.

Vytvoří se plán fakturace, který má následující kritéria:

- **Počáteční datum:** 1. června 2020
- **Koncové datum:** 31. prosince 2021
- **Jednotková cena** $100
- **Frekvence:** měsíčně

Na stránce **Všechny plány fakturace** je počáteční položka deníku vytvořena procesem **Vytvořit deníkovou položku**. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $700
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $1,200

Faktura je vystavena za fakturační období od 1. června 2020 do 30. listopadu 2020. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $100
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $1,200

Faktura je vystavena za fakturační období od 1. prosince 2020 do 31. prosince 2020. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $1,200
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $0

#### <a name="short-term-rolling-periods"></a>Krátkodobé: Klouzavá období

Chcete-li použít nevyfakturované výnosy s krátkodobou funkcí, nastavte hodnotu v poli krátkodobé nefakturované na stránce **Parametry opakované fakturace smlouvy**. Následující příklad ukazuje výpočty, které se provádějí při použití nevyfakturovaných výnosů spolu s metodou **Období prosazení** pro krátkodobé nevyfakturované výnosy.

Vytvoří se plán fakturace, který má následující kritéria:

- **Počáteční datum:** 1. června 2020
- **Koncové datum:** 31. prosince 2021
- **Jednotková cena** $100
- **Frekvence:** měsíčně

Na stránce **Všechny plány fakturace** je počáteční položka deníku vytvořena procesem **Vytvořit deníkovou položku**. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $1,200
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $700

Faktura je vystavena za fakturační období od 1. června 2020 do 30. listopadu 2020. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $1,200
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $100

Faktura je vystavena za fakturační období od 1. prosince 2020 do 31. prosince 2020. Aktuální krátkodobé a dlouhodobé částky se počítají takto:

- **Aktuální částka krátkodobých nevyfakturovaných příjmů:** $1,200
- **Aktuální částka dlouhodobých nevyfakturovaných příjmů:** $0

### <a name="items-with-revenue-allocation"></a>Položky s alokací výnosů

Do rozvrhu účtování jsou přidány dvě položky, které mají různé frekvence fakturace. Oba používají nevyfakturované výnosy a jsou odloženými položkami.

- **Číslo položky 1000:** Surface Pro 128 GB

    - **Frekvence fakturace:** jednorázová
    - **Jednotková cena** $1,500
    - **Samostatná prodejní cena:** $1,600
    - **Výnosy smlouvy:** $1,465.26

- **Číslo položky S0021:** Pojištění, které se prodává společně s položkou číslo 1000

    - **Frekvence účtování:** Měsíčně po dobu 12 měsíců
    - **Jednotková cena:** $20 měsíčně
    - **Samostatná prodejní cena:** $25
    - **Výnosy smlouvy:** $264.74

Protože obě položky využívají nevyfakturované příjmy a alokaci příjmů, je celková částka smlouvy na řádku obnovení 0 (nula). Sloupec **Výnos ze smlouvy** je přidán a zobrazuje částku smluvního výnosu.

Následující tabulka ukazuje počáteční zápis do deníku pro položky a fakturu.

| Účet nevyfakturovaných výnosů | Účet odložených výnosů | Částka Má dáti | Částka Dal |
|---|---|---|---|
| **Typ položky 1000 deníku** | | | |
| Na vrub účtu nevyfakturovaných výnosů (401250) | | $1,465.26 | |
| | Účet výnosů odloženého kreditu (250600) | | $1,465.26 |
| **Položka 0021 deníku** | | | |
| Na vrub účtu nevyfakturovaných výnosů (401250) | | $274.74 | |
| | Účet výnosů odloženého kreditu (250600) | | $274.74 |
| **Faktura** | | | |
| | Kreditní účet nevyfakturovaných výnosů | | $1,465.26 |
| | Kreditní účet nevyfakturovaných výnosů | | $274.74 |
| Debetní účet AR (130100) | | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Změny řádku plánu vyúčtování, řádku detailu vyúčtování nebo rozdělení příjmů

Při změně jednotkové ceny nebo množství je třeba aktualizovat částku příjmů ze smlouvy pro každou položku, která je součástí alokace příjmů. Proto se položka deníku přepočítá.

Například jednotková cena položky 1000 se změní z $1,500 na $1,600. V tomto případě se částka výnosu ze smlouvy automaticky přepočítá jako $1,549.47. Výnos ze smlouvy pro položku S0021 se přepočítá jako $290.53.

Když je změna potvrzena a odevzdána, původní záznamy v deníku pro obě položky se stornují a vytvoří se nové záznamy v deníku:

- **Položka 1000:** Původní počáteční položka deníku $1,465.26 je stornována. Vytvoří se nová položka deníku na částku 1 549,47 USD.
- **Položka S0021:** Původní počáteční položka deníku $274.74 je stornována. Vytvoří se nová položka deníku na částku 1 549,47 USD.

#### <a name="termination"></a>Ukončení

Položka S0021 má datum zahájení v lednu 2020 a datum ukončení v prosinci 2020, ale je ukončena v červnu 2020. Výše výnosů ze smlouvy pro obě položky musí být přepočítána:

- **Položka 1000:** Výnos ze smlouvy pro položku S0021 se přepočítá jako $1,567.67.
- **Položka S0021:** Výnos ze smlouvy pro položku S0021 se přepočítá jako $124.00.

Pro ukončený řádek se vytvoří opravná položka deníku. Položka deníku pro řádek, který patří ke stejnému číslu uspořádání více prvků (MEA), se zruší a vytvoří se nový záznam v deníku:

- **Položka 1000:** Původní počáteční položka deníku $1,465.26 je stornována. Vytvoří se opravná položka deníku na částku 1 549,47 USD.
- **Položka S0021:** Původní počáteční položka deníku $274.74 je stornována. Vytvoří se nová položka deníku na částku $124.00.
