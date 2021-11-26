---
title: Plánování na základě priority
description: Toto téma popisuje funkci plánování na základě priority v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 41c4f3e9bd41735b213743bd8b4cdd8d9657a073
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777882"
---
# <a name="priority-based-planning"></a>Plánování na základě priority

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Toto téma popisuje funkci plánování na základě priority v softwaru Microsoft Dynamics 365 Supply Chain Management. Tato funkce přidává podporu pro plánování řízené poptávkou, což je jeden z kroků plánování materiálových požadavků řízené poptávkou (DDMRP). Plánování na základě priority umožňuje nástroji Optimalizace plánování generovat plánované objednávky, které jsou řízeny prioritami plánování namísto dat požadavků.

Plánování na základě priority vám umožňuje upřednostňovat objednávky na doplnění, abyste zajistili, že naléhavá poptávka bude upřednostněna před méně důležitou poptávkou. Například objednávka na doplnění vyčerpaných zásob bude mít přednost před standardní objednávkou na doplnění zásob. Systém dokáže automaticky rozdělit větší objednávky na samostatné menší objednávky, kde jsou řádky objednávek seskupeny podle priority. Poté může nejprve zpracovat všechny objednávky s vysokou prioritou.

Chcete-li získat rychlý přehled o této funkci, podívejte se na následující video: [Podpora optimalizace plánování u plánování na základě priority v Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Zapnutí plánování na základě priority v systému

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Hlavní plánování*
- **Název funkce:** *Podpora MRP řízená prioritou pro Optimalizaci plánování*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Kde a jak jsou přiřazeny priority plánování

Informace *Priority plánování* o nabídce a poptávce jsou základem plánování založeného na prioritách. Priorita plánování definuje důležitost řádku poptávky nebo nabídky. Optimalizace plánování jej používá, když je pole **Kód disponibility** nastaveno na *Priorita*.

Priorita plánování je obvykle číslo mezi 0 (nulou) a 100, kde 0 představuje nejvyšší důležitost. Je zobrazena a nastavena v poli **Priorita plánování**. Toto pole naleznete na následujících stránkách: **Řádky prognózy poptávky**, **Podrobnosti prodejní objednávky**, **Podrobnosti nákupní objednávky**, **Podrobnosti převodního příkazu** a **Podrobnosti plánované objednávky**.

Když je pole **Kód disponibility** pro příslušnou položku nebo skupinu pokrytí nastaveno na *Prioritu*, Optimalizace plánování vyvažuje nabídku a poptávku pomocí přístupu řízeného poptávkou, protože vypočítá prioritu plánování a pro každý uvolněný produkt zvažuje hodnoty, které jsou nastaveny v polích **Minimální**, **Bod přiobjednání** a **Maximum** na stránce **Disponibilita položky**.

> [!NOTE]
> Hodnota *Priorita* je pro pole **Kód disponibility** k dispozici pouze v případě, že je povolena Optimalizace plánování.

Související *modely plánování na základě priority* řídí prioritu plánování a rozdělují plánované objednávky podle rozsahu priorit. Umožňují vám také nastavit výchozí hodnoty priority plánování pro každý typ nabídky nebo poptávky a definovat metodu výpočtu priority.

## <a name="types-of-priority-calculation-methods"></a>Typy metod výpočtu priority

Každý model priority plánování má nastavení **Metoda výpočtu priority**, které řídí, jak hlavní plánování aplikuje prioritu na plánované objednávky. Dostupné hodnoty jsou *Procento maximálního množství zásob* a *Rozsahy priorit*. Hodnota *Rozsahy priorit* představuje pokročilejší verzi metody *Procento maximálního množství zásob*.

### <a name="percent-of-maximum-inventory-quantity"></a>Procento maximálního množství zásob

V metodě výpočtu *Procento maximálního množství zásob* najde výpočet priority dodávky aktuální *celkové dostupné zásoby* (čistý tok) jako procento hodnoty **Maximální skladové množství**, která je nastavena pro položku. Potom se vytvoří jedna plánovaná objednávka na položku a dodavatele (pokud není k vynucení rozdělení použito maximální množství objednávky). Priorita plánování objednávky se vypočítá jako procento z maxima.

Použije se následující vzorec:

*Procento maxima* = (*Poloha čistého toku* × 100) ÷ *Maximální hodnota množství zásob z disponibility položky*

V tomto vzorci je *Poloha čistého toku* počítána následujícím způsobem:

*Poloha čistého toku* = *Na skladě* + *Na objednávce* – *Kvalifikovaná poptávka*

- *Na objednávce* je očekávaná nabídka.
- *Kvalifikovaná poptávka* představuje čisté požadavky, které mají datum požadavku v rámci časového ohraničení plánování.

Během spuštění hlavního plánování se vytvářejí nové plánované objednávky, když je pozice čistého toku menší než množství bodu přiobjednání pro položku. Množství plánované objednávky je rozdíl mezi hodnotou **Maximální skladové množství**, která je nastavena na úrovni položky, a pozicí čistého toku. Priorita plánované objednávky se vypočítá jako procento *pozice čistého toku* z hodnoty **Maximální skladové množství**.

> [!NOTE]
> Vypočtená priorita nemůže být záporná, i když poptávka převyšuje celkovou nabídku. Pokud poptávka převyšuje celkovou nabídku, vypočítaná priorita je nastavena na 0 (nula).

### <a name="priority-ranges"></a>Rozsahy priorit

Metoda výpočtu *Rozsahy priorit* je propracovanější než metoda *Procento maximálního množství zásob* a je konfigurována na úrovni modelu priorit plánování. Pro uspokojení poptávky na položku lze vytvořit několik nových plánovaných objednávek dodávek. Priority plánované dodávky se řídí hodnotami, které jsou definovány v mřížce **Rozsahy priorit plánování** na stránce **Modely priority plánování**.

Následující doplňková pravidla začnou platit, když je pole **Metoda výpočtu priority** nastaveno na *Rozsahy priorit*:

- Pokud je možnost **Zvážit prioritu poptávky** pro model priority plánování nastavena na *Ano*, omezí priorita nastavená na každém řádku poptávky rozsah priorit. Priorita jakékoli nové plánované objednávky pro dodávku nebude nižší než priorita poptávky. Horní hodnota rozsahu je považována za prahovou hodnotu, se kterou se porovnává hodnota priority poptávky. Pokud je priorita poptávky přesně uprostřed mezi horními prahovými hodnotami dvou rozsahů, bude vybrán rozsah, který má nejvyšší prioritu (tj. nejnižší hodnotu priority).
- Pokud je pole **Vytvoření plánované objednávky** pro model priority plánování nastaveno na *Jedna dodávka s nejdůležitější prioritou*, bude vytvořena pouze jedna dodávka, která splní celou poptávku až do maxima. Priorita bude nastavena na prioritu prvního rozsahu, který spustí dodávku.
- Pokud není k dispozici žádné množství na skladě, žádná nabídka ani poptávka, bude použit ten řádek v mřížce **Rozsahy priorit plánování**, který má pole **Od množství** nastaveno na *Nula*.
- Pokud existuje poptávka, ale není k dispozici žádné množství na skladě nebo očekávaná dodávka, bude použit ten řádek v mřížce **Rozsahy priorit plánování**, který má pole **Od množství** nastaveno na *Nula nebo menší*.
- Když se vyhodnotí rozsah, jehož je poptávka součástí, nastavení možnosti **Zvážit prioritu poptávky** bude stále účinkovat.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Rozdíly mezi tradičními výpočty na časové ose a plánováním založeným na prioritách

Plánování založené na prioritách se liší od tradičních výpočtů na časové ose následujícími způsoby:

- Všechny běžné procesory předběžného plánování stále platí. Tyto preprocesory zahrnují doložení schválených plánovaných objednávek proti prodejní poptávce, mapování nákupních požadavků a rezervační logiku. Zpracovává se pouze poptávka, která není splněna těmito preprocesory.
- Během doložení se bere v úvahu veškerá dodávka bez ohledu na její prioritu. Tato dodávka zahrnuje zásoby na skladě, uvolněnou dodávku a nedoloženou část schválených plánovaných objednávek.
- Po celou dobu disponibility nelze doložit poptávku „záporných dnů“ vůči dodávce.
- Když je dodávka doložena vůči poptávce, je jako první spotřebována dodávka, která má nejvyšší prioritu (tj. nejnižší hodnotu priority). Zásoby na skladě mají hodnotu priority 0 (nula). Proto budou spotřebovány jako úplně první zdroj.
- Nové řádky plánované dodávky budou vytvořeny podle běžných pravidel pro minimální velikost objednávky, maximální velikost objednávky, násobek množství a tak dále.

## <a name="planning-priority-models"></a>Modely priority plánování

*Modely priority plánování* jsou přiřazeny ke skupinám disponibility a řídí prioritu plánování u plánovaných objednávek. Definují logiku, která určuje, jak se pro každou plánovanou objednávku vypočítá hodnota priority plánování, a jak se priorita přiřadí plánovaným objednávkám, řádkům dodávky a řádkům poptávky.

Chcete-li pracovat s modely priorit plánování, přejděte na **Hlavní plánování \> Nastavení \> Modely priority plánování**. Jak již bylo zmíněno, jedním z nejdůležitějších nastavení modelu je hodnota **Metoda výpočtu priority**. Toto nastavení řídí metodu výpočtu, která se používá, když hlavní plánování přiřazuje hodnotu priority plánovaným objednávkám.

> [!NOTE]
> Modely priorit plánování platí v celé organizaci, napříč všemi právnickými osobami.

### <a name="coverage-group"></a>Skupina disponibility

Nastavte novou skupinu disponibility, kterou plánujete použít pro plánování na základě priorit, jak je popsáno v tématu [Definování pravidel disponibility pro položky](../tasks/define-coverage-rules-items.md). Po vytvoření skupiny disponibility nastavte následující další pole:

- **Kód disponibility** – Vyberte *Priorita*, pokud bude skupina disponibility používat plánování založené na prioritách.
- **Model priorit plánování** – Vyberte jakýkoli model priorit plánování pro celou organizaci.

### <a name="item-coverage"></a>Disponibilita položky

Upravte nastavení disponibility položek, jak je popsáno v tématu [Nastavení disponibility](../coverage-settings.md). Ve výchozím nastavení se hodnota **Kód disponibility**, která je vybraná pro skupinu disponibility, zkopíruje do nastavení disponibility položky. Výchozí hodnotu však můžete podle potřeby přepsat. V některých případech je pole **Kód disponibility** pro záznam disponibility položky nastaveno na *Plánování*, ale pro související skupinu disponibility není definován žádný model priority plánování. V těchto případech bude jakýkoli model, kde je pole **Metoda výpočtu priority** nastaveno na *Procento maximálního množství zásob* a pole **Vytvoření plánované objednávky** na *Jedna dodávka s nejdůležitější prioritou*, použit jako výchozí.

Nastavte pole **Kód disponibility** na *Priorita*, aby bylo v nastavení disponibility položky dostupné pole **Bod přiobjednání**. Do tohoto pole zadejte množství bodu přiobjednání, které by měl systém použít při určování, kdy zadat plánované objednávky, u kterých má pole **Kód disponibility** hodnotu *Priorita*.

Množství bodu přiobjednání se často počítá jako poptávka během doby realizace plus minimální hodnota (bezpečnostní zásoba). Musí to být hodnota mezi **Minimem** a **Maximem**.

Pole můžete nastavit například následujícím způsobem:

- **Minimum:** *10*
- **Bod přiobjednání:** *45*
- **Maximum:** *60*

V tomto příkladu je množství bodu přiobjednání založeno na době realizace sedm dní a průměrném denním využití 5. Proto je poptávka během doby realizace 35. Minimální hodnota 10 (bezpečnostní zásoba) je poté přičtena, abyste získali bod přiobjednání s hodnotou 45. Při použití tohoto nastavení bude dodávka navržena, když je očekávané množství na skladě nižší než 45. Priorita objednávky bude vycházet z nastavení priority plánování.

### <a name="manage-planning-priority-models"></a>Správa modelů priorit plánování

Chcete-li pracovat s modely priorit plánování, postupujte následovně.

1. Přejděte na **Hlavní plánování \> Nastavení \>Modely priorit plánování**.
1. Buď vyberte existující model v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte nový model.
1. V záhlaví záznamu nastavte následující pole:

    - **Název** – Zadejte název modelu. Název musí být jedinečný v rámci všech právnických osob ve vaší organizaci.
    - **Popis** – Zadejte popis modelu.
    - **Metoda výpočtu priority** – Vyberte jednu z následujících hodnot:

        - *Rozsahy priorit* – Když vyberete tuto hodnotu, bude k dispozici mřížka **Rozsahy priorit plánování**. Zde musíte stanovit několik rozsahů priorit, abyste mohli definovat hodnotu priority plánování.
        - *Procento maximálního množství zásob* – Vypočítejte hodnotu priority plánování jako procento na základě projektované úrovně zásob nad maximálním množstvím zásob.

    - **Vytvoření plánované objednávky** – Toto pole je dostupné, když je **Metoda výpočtu priority** nastavena na *Rozsahy priorit*. Vyberte jednu z následujících hodnot:

        - *Jedna dodávka s nejdůležitější prioritou* – Nerozdělovat plánované objednávky na základě rozsahu priorit. Priorita plánování pro plánovanou objednávku je založena na nejdůležitějším rozsahu priorit (tj. na nejnižší hodnotě priority plánování).
        - *Rozdělit podle rozsahů priorit* – Rozdělit poptávku do více plánovaných objednávek na základě rozsahů priorit plánování. Priorita plánování pro jednotlivé plánované objednávky je definována prioritou plánování příslušného rozsahu priorit plánování.

    - **Zvážit prioritu poptávky** – Nastavte tuto možnost na *Ano*, když chcete omezit prioritu nové plánované objednávky, která je vytvořena pro dodávku. (Priorita nebude nižší než priorita související poptávky.) Pokud tuto možnost nastavíte na *Ne*, priorita objednávky poptávky nebude při výpočtu priority objednávky dodávky brána v úvahu.

1. Pokud nastavíte pole **Metoda výpočtu priority** na *Rozsahy priorit*, použijte tlačítka **Přidat** a **Odebrat** na panelu nástrojů v záložce s náhledem **Rozsahy priorit plánování** k přidání nebo odebrání řádků rozsahu priorit. Pokud existuje více řádků a vložíte nový řádek, priorita plánování se automaticky nastaví na průměr vybraného řádku a řádku nad ním. Pro každý řádek je třeba nastavit tato pole:

    - **Priorita plánování** – Zadejte libovolnou hodnotu mezi 0,00 a 100,00. Tato hodnota představuje prioritu plánování, která se používá pro řádek. Nejnižší hodnota priority reprezentuje nejvyšší prioritu. Je přiřazena výchozí hodnota, můžete ji však podle potřeby změnit. Stejnou hodnotu **Priorita plánování** nelze použít pro více než jeden rozsah priorit plánování ve stejném modelu priorit plánování.
    - **Popis** – Zadejte popis rozsahu priorit plánování (jako např *Bod přiobjednání až maximum*).
    - **Od množství** – Spodní mez rozsahu priorit plánování. Tato hodnota je pouze ke čtení a je založena na hodnotách **Do množství** a **Procento do množství** pro předchozí rozsah priorit plánování.
    - **Do množství** – Vyberte pole z disponibility položky, které by se mělo použít k definování horní hranice rozsahu. Následující hodnoty jsou podporované a ovlivní hodnotu **Od množství** dalšího rozsahu:

        - *Nula* – Tato hodnota představuje záporný až nulový rozsah (*Nula nebo méně* až *Nula*). U řádků, kde je tato hodnota vybrána, je pole **Procento do množství** pouze ke čtení a je vždy nastaveno na *100* procent.
        - *Minimální skladové množství* – Tato hodnota představuje **Minimum** pro položku na stránce **Disponibilita položky**. U řádků, kde je tato hodnota vybrána, je pole **Procento do množství** upravitelné a používá se k nastavení hodnoty **Od množství** dalšího rozsahu (například na *80 % minimálního množství zásob*).
        - *Bod přiobjednání* – Tato hodnota představuje hodnotu **Bodu přiobjednání** pro položku na stránce **Disponibilita položky**. U řádků, kde je tato hodnota vybrána, je pole **Procento do množství** upravitelné a používá se k nastavení hodnoty **Od množství** dalšího rozsahu (například na *80 % bodu přiobjednání*).
        - *Maximální skladové množství* – Tato hodnota představuje **Maximum** pro položku na stránce **Disponibilita položky**. U řádků, kde je tato hodnota vybrána, je pole **Procento do množství** upravitelné a používá se k nastavení hodnoty **Od množství** dalšího rozsahu (například na *80 % minimálního množství zásob*).
        - *Nekonečno* – Tato hodnota představuje nekonečnou horní úroveň rozsahu (*Nekonečno nebo méně* až *Nekonečno*). U řádků, kde je tato hodnota vybrána, je pole **Procento do množství** pouze ke čtení a je vždy nastaveno na *100* procent.

    - **Procento do množství** – Zadejte procentuální hodnotu, která se použije k výpočtu horní hranice rozsahu priorit plánování na základě hodnoty, která je vybrána v poli **Do množství**. Například, pokud je pole **Do množství** nastaveno na *Minimální skladové množství* a pole **Procento do množství** je nastaveno na *50*, horní limit bude 50 procent minimálního množství zásob z disponibility související položky.

1. Na záložce s náhledem **Výchozí nastavení priority plánování** nastavte podle potřeby pole k definování výchozích priorit plánování pro každý typ řádku dodávky nebo poptávky (prodejní objednávka, nákupní objednávka, převodní příkaz nebo prognóza poptávky). Lze zadat pouze kladné hodnoty.

## <a name="view-and-maintain-planning-priority"></a>Zobrazení a údržba priorit plánování

Priorita plánování je zobrazena a nastavena v poli **Priorita plánování**. Toto pole naleznete na stránkách, které jsou uvedeny v následující tabulce. Priorita plánování je nastavena číslo mezi 0 (nulou) a 100, kde 0 představuje nejvyšší důležitost.

| Strana | Skladové místo | Zdroj hodnoty |
|---|---|---|
| Řádky prognózy poptávky | <p>Karta **Položka**</p><p>(Vyberte řádek v horní části a poté vyberte kartu **Položka**.)</p> | Výchozí hodnota nebo hodnota, která se nastavuje ručně |
| Detaily prod. objednávky | <p>Karta **Dodání** na záložce s náhledem **Detaily řádku**</p><p>(Vyberte řádek na záložce s náhledem **Řádky prodejní objednávky** a poté na záložce s náhledem **Detaily řádku** vyberte kartu **Dodání**.)</p> | Výchozí hodnota, hodnota z mezipodnikového obchodu, nebo hodnota, která se nastavuje ručně |
| Podrobnosti nákupní objednávky | <p>Karta **Dodání** na záložce s náhledem **Detaily řádku**</p><p>(Vyberte řádek na záložce s náhledem **Řádky nákupní objednávky** a poté na záložce s náhledem **Detaily řádku** vyberte kartu **Dodání**.)</p> | Hodnota, která se nastavuje při potvrzování z plánovaných objednávek, hodnota z mezipodnikového obchodu nebo hodnota, která se nastavuje ručně |
| Detaily převodního příkazu | <p>Karta **Dodání** na záložce s náhledem **Detaily řádku**</p><p>(Vyberte řádek na záložce s náhledem **Řádky převodního příkazu** a poté na záložce s náhledem **Detaily řádku** vyberte kartu **Dodání**.)</p> | Hodnota, která se nastavuje při potvrzování z plánovaných objednávek, nebo hodnota, která se nastavuje ručně |
| Podrobnosti o plánované objednávce | Záložka s náhledem **Obecné** | Hodnota, která se vypočítá během hlavního plánování, nebo hodnota, která se nastaví ručně |

### <a name="intercompany-trade"></a>Mezipodnikový obchod

**Priorita plánování** na řádcích mezipodnikových dodávek a poptávek je sdílena mezi propojenými subjekty. Úprava na obou stranách se projeví na propojeném řádku objednávky.

Několik příkladů:

- Uživatel změní prioritu plánování pro řádek mezipodnikové prodejní objednávky z 20 na 30. Tato změna se projeví na řádku propojené mezipodnikové nákupní objednávky.
- Uživatel změní prioritu plánování pro řádek mezipodnikové nákupní objednávky z 40 na 50. Tato změna se projeví na řádku propojené mezipodnikové prodejní objednávky.
